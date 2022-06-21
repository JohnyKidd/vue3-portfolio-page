<script setup>
import Greeting from './components/Greeting.vue';
import SliderTech from './components/SliderTech.vue';
import Project from './components/Project.vue';

const technologies = [
    "../src/assets/imgs/html.svg",
    "../src/assets/imgs/css.svg",
    "../src/assets/imgs/js.svg",
    "../src/assets/imgs/mysql.svg",
    "../src/assets/imgs/php.svg",
    "../src/assets/imgs/vue.svg",
];

const projects = [
    {
        name: "Simple Todo list application with Vue",
        image: "../src/assets/projects/todo.png",
        codeLink: "https://github.com/JohnyKidd/vue-3-practice-todo-list-app",
        siteLink: "https://johnykidd.github.io/vue-3-practice-todo-list-app/"
    },
    {
        name: "Catmash - facemash clone in PHP and mySQL",
        image: "../src/assets/projects/catmash.png",
        codeLink: "https://github.com/JohnyKidd/catmash-facemash-clone-practice-project-",
    },
    {
        name: "A Star Wars themed fantasy landing page",
        image: "../src/assets/projects/swlanding.png",
        codeLink: "https://github.com/JohnyKidd/SW3-3D-fantasy-landing-page",
        siteLink: "https://johnykidd.github.io/SW3-3D-fantasy-landing-page/"
    }
]
</script>

<template>
    <div class="grid-container">
        <Greeting />
        <h2>Technologies I work with:</h2>
        <div class="flex-container">
            <SliderTech :technologies="technologies" />
        </div>
        <h2>My Projects:</h2>
        <Project :projects="projects" />
    </div>
</template>

<style scoped>
 @import url('https://fonts.googleapis.com/css2?family=Chakra+Petch:wght@500&display=swap');
*{
        font-family: 'Chakra Petch', sans-serif;
}
.grid-container{
    display: grid;
    place-items: center;
}
h2{
    margin-top: 1em;
    margin-bottom: 1em;
}
.flex-container{
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    gap: 1em;
    margin-top: 2em;
}
</style>