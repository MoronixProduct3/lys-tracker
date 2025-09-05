<template>
    <v-dialog v-model="dialog" max-width="600">
        <template v-slot:activator="{ props: activatorProps }">
            <v-btn v-if="online" variant="text" prepend-icon="mdi-lan-connect" v-bind="activatorProps">
                <template v-slot:prepend>
                    <v-icon color="success"></v-icon>
                </template>
                Connected
            </v-btn>
            <v-btn v-else variant="text" color="red" prepend-icon="mdi-lan-disconnect" v-bind="activatorProps">
                Connection broken
            </v-btn>
        </template>

        <v-card prepend-icon="mdi-sword" title="BCP Event">
            <v-card-text>
                <v-text-field label="Event" v-model="event" clearable></v-text-field>
                <v-text-field disabled label="Auth Token" clearable></v-text-field>
            </v-card-text>
            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn text="Test" @click="fetchData"></v-btn>
                <v-btn text="Close" @click="dialog = false"></v-btn>
            </v-card-actions>
        </v-card>
    </v-dialog>

    <v-btn @click="fetchData" variant="text" icon="mdi-refresh"></v-btn>
</template>

<script setup>
import { ref , onMounted, onBeforeUnmount} from 'vue'

const dialog = ref(false)
const event = ref("wf32USYfefge")
const online = ref(false)

const emit = defineEmits(['incoming'])

async function fetchData() {
    try {
        const response = await fetch('https://newprod-api.bestcoastpairings.com/v1/events/' + event.value,
            {
                headers: {
                    "client-id": "web-app",
                },
            }
        )

        if (!response.ok) {
            online.value = false
            return
        }

        const js = await response.json()
        emit('incoming', js)
        online.value = true

    } catch (error) {
        console.error(error)
        online.value = false
    }
}

let intervalId

function startPolling() {
    fetchData()
    intervalId = setInterval(fetchData, 60000);
}

function stopPolling() {
    clearInterval(intervalId)
}

onMounted(startPolling)
onBeforeUnmount(stopPolling)

</script>