<template>
    <p contenteditable class="text-h1 text-red-lighten-1" :class="{ 'text-grey-darken-3': disable_message }"
        @input="updateMessage" @blur="resetMessage" @focus="editMessage">
        {{ defaultMessage }}
    </p>
</template>

<script setup>
import { ref } from 'vue'

const defaultMessage = '...'
const disable_message = ref(true)

function updateMessage(event) {
    disable_message.value = event.target.textContent === defaultMessage
}

function resetMessage(event) {
    if (event.target.textContent === "") {
        event.target.textContent = defaultMessage
        disable_message.value = true
    }
}

function editMessage(event) {
    if (event.target.textContent === defaultMessage) {
        event.target.textContent = ""
    }
}
</script>
