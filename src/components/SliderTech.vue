<script setup>
const props = defineProps({
    technologies: {
        type: Array,
        required: true
    }
})
</script>

<template>
<div v-for="tech in technologies">
    <img :src="tech" class="tech-image">
</div>
</template>

<style scoped>
.tech-image{
    max-width: 100px;
    border: 1px solid black;
    border-radius: 10px;
    padding: .5em;
    min-height: 100px;
}
</style>