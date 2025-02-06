<template>
    <h4>{{ m.name }}:</h4>
    <v-img :src=m.image></v-img>
</template>

<script setup>
defineProps({
    m: {
        require: true
    }
})

</script>