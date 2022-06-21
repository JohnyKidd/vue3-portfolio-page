<script setup>
import Greeting from './components/Greeting.vue';
import SliderTech from './components/SliderTech.vue';
import Project from './components/Project.vue';
import Contact from './components/Contact.vue';

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
        siteLink: "https://johnykidd.github.io/vue-3-practice-todo-list-app/",
        id: 1
    },
    {
        name: "Catmash - facemash clone in PHP and mySQL",
        image: "../src/assets/projects/catmash.png",
        codeLink: "https://github.com/JohnyKidd/catmash-facemash-clone-practice-project-",
        id: 2
    },
    {
        name: "A Star Wars themed fantasy landing page",
        image: "../src/assets/projects/swlanding.png",
        codeLink: "https://github.com/JohnyKidd/SW3-3D-fantasy-landing-page",
        siteLink: "https://johnykidd.github.io/SW3-3D-fantasy-landing-page/",
        id: 3
    },
    {
        name: "A simple weather application",
        image: "../src/assets/projects/weather.png",
        codeLink: "https://github.com/JohnyKidd/weatherapp_javascript",
        siteLink: "https://johnykidd.github.io/weatherapp_javascript/s",
        id: 4
    },
    {
        name: "Application for counting calories (In progress)",
        image: "../src/assets/projects/nutritio.png",
        codeLink: "https://github.com/JohnyKidd/nutritio",
        siteLink: "https://johnykidd.github.io/nutritio/",
        id: 5
    },
    {
        name: "A little tic-tac-toe game",
        image: "../src/assets/projects/tictactoe.png",
        codeLink: "https://github.com/JohnyKidd/tictactoe_javascript",
        siteLink: "https://johnykidd.github.io/tictactoe_javascript/",
        id: 6
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
        <div class="project-grid">
            <Project :projects="projects" />
        </div>
        <Contact />
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
@media (min-width: 40em) {
   .project-grid{
    display: grid;
    grid-template-columns: repeat(2, 50%);
} 
}

h2{
    margin-top: 1em;
    margin-bottom: 1em;
}
.flex-container{
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    gap: 2em;
    margin-top: 2em;
}
</style>