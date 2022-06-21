<script setup>
const props = defineProps({
    projects: {
        type: Array,
        required: true
    }
})
</script>

<template>
<div
class="flex-projects"
v-for="project in projects"
:key="project.id"
>

    <h3>{{ project.name }}</h3>
    <img :src="project.image" alt="">
    <div class="navigation-projects">
        <a v-if="project.codeLink" class="project-links" :href="project.codeLink" target=”#”>Code</a>
        <a v-if="project.siteLink" class="project-links" :href="project.siteLink" target=”#”>Site</a>
    </div>

</div>

</template>

<style scoped>
@keyframes slideInFromBottom {
  0% {
    transform: translateY(100vw);
  }
  100% {
    transform: translateX(0);
  }
}
.flex-projects{
    display: flex;
    flex-flow: column wrap;
    align-items: center;
    justify-content: center;
    gap: 1em;
    animation: 2s ease-out 0s 1 slideInFromBottom;
    padding: 1em;
    border: 5px solid #000;
    border-radius: 15px;
    background: #9DFFD7;
    margin: 1em;
}
.navigation-projects{
    display: flex;
    flex-flow: row wrap;
    gap: 5em;
}
.project-links{
    text-decoration: none;
    padding: 1em;
    width: 80px;
    text-align: center;
    background: #000;
    color: #fff;
    border-radius: 10px;
    transition: all 200ms;
}
.project-links:hover{
    transform: scale(1.1);
    background: #444;
}
img{
    max-width: 400px;
    border: 5px solid #000;
    border-radius: 10px;
}
h3{
    margin-top: 2em;
    margin-bottom: 2em;
}
</style>