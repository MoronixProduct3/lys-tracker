<template>
    <h4>{{ r.name }}:</h4>
    <p v-html=r.text></p>
</template>

<script setup>
defineProps({
    r: {
        require: true
    }
})

</script>