<script setup>
const props = defineProps({
    technologies: {
        type: Array,
        required: true
    }
})
</script>

<template>
<div
v-for="tech in technologies"
>
    <img
    :src="tech"
    class="tech-image">
</div>
</template>

<style scoped>
@keyframes topSlide {
  0% {
    transform: translateY(-100vh);
  }
  25%{
    transform: scale(0.5);
  }
  50%{
    transform: translateX(0);
  }
  100% {
    transform: scale(1);
  }
}
.tech-image{
    max-width: 125px;
    border: 5px solid black;
    border-radius: 10px;
    padding: 1em;
    min-height: 125px;
    animation: 2s ease-out 0s 1 topSlide;
    background: #fff;
}
</style>