<template>
    <v-container ref="el">
        <v-row>
            <v-col class="text-end" cols="12">
                <BcpConnector @incoming="incomingData" />
            </v-col>
            <v-col class="text-center" cols="12">
                <div v-resize-text="{ ratio: 0.55 }">
                    {{ time }}
                </div>
            </v-col>
            <v-col class="text-center" cols="12">
                <h1 class="text-h2">Round {{ round_n }}</h1>
            </v-col>
            <v-col class="text-center" cols="12">
                <DisplayMessage />
            </v-col>
            <v-col class="text-center" cols="6">
                <!-- <h2>mission</h2> -->
            </v-col>
            <v-col class="text-center" cols="6">
                <!-- <h2>map</h2> -->
            </v-col>
        </v-row>
    </v-container>
    <button @click="toggle">
        Go Fullscreen (F)
    </button>
</template>

<script setup>
import { useFullscreen } from '@vueuse/core'
import { useTemplateRef, onMounted, onUnmounted, ref } from 'vue'

let intervalId

onMounted(() => {
    document.addEventListener('keydown', globalKeydownHandler)
    intervalId = setInterval(refreshTime, 1000);
})
onUnmounted(() => {
    document.removeEventListener('keydown', globalKeydownHandler)
    clearInterval(intervalId)
})

const el = useTemplateRef('el')
const { toggle } = useFullscreen(el)

function globalKeydownHandler(event) {
    if (event.key === 'f') {
        toggle()
    }
}

const time = ref('00:00:00')
const round_n = ref(1)
const round_end = ref(0)

function refreshTime() {
    const now = Date.now()
    const left = Math.max(round_end.value - now, 0)

    const hours = Math.floor(left / 3600000)
    const mins = Math.floor((left % 3600000) / 60000)
    const secs = Math.floor((left % 60000) / 1000)

    const pad = (num) => String(num).padStart(2, '0')
    time.value = `${pad(hours)}:${pad(mins)}:${pad(secs)}`
}

function incomingData(js) {

    const timers = js.roundTimers

    var nextRoundEnd = Number.MAX_SAFE_INTEGER
    var round = -1
    var maxRound = Number.MIN_SAFE_INTEGER
    const now = Date.now()

    for (const tn in timers) {
        maxRound = Math.max(maxRound, tn)
        const end = Date.parse(timers[tn].endTime)
        if (now > end) continue;

        if (end < nextRoundEnd) {
            nextRoundEnd = end
            round = tn
        }
    }

    if (round === -1) {
        round_n.value = maxRound
        round_end.value = 0
        return
    }

    round_n.value = round
    round_end.value = nextRoundEnd
}

</script>
