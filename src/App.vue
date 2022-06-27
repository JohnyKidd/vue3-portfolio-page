<script setup>
// components
import Greeting from './components/Greeting.vue';
import SliderTech from './components/SliderTech.vue';
import Project from './components/Project.vue';
import Contact from './components/Contact.vue';
import Personal from './components/Personal.vue';

// tech images
import htmlImage from './assets/imgs/html.svg';
import cssImage from './assets/imgs/css.svg';
import jsImage from './assets/imgs/js.svg';
import sqlImage from './assets/imgs/mysql.svg';
import phpImage from './assets/imgs/php.svg';
import vueImage from './assets/imgs/vue.svg';

// tool images
import psImage from './assets/tools/photoshop.svg';
import ghImage from './assets/tools/github.svg';
import tailwindImage from './assets/tools/tailwind.svg';
import viteImage from './assets/tools/vite.svg';
import vscodeImage from './assets/tools/vscode.svg';
import webpackImage from './assets/tools/webpack.svg';

// project images
import todoImage from './assets/projects/todo.png';
import catmashImage from './assets/projects/catmash.png';
import swImage from './assets/projects/swlanding.png';
import weatherImage from './assets/projects/weather.png';
import nutritioImage from './assets/projects/nutritio.png';
import tictactoeImage from './assets/projects/tictactoe.png';

const technologies = [
    htmlImage,
    cssImage,
    jsImage,
    sqlImage,
    phpImage,
    vueImage
];

const tools = [
    psImage,
    ghImage,
    tailwindImage,
    viteImage,
    vscodeImage,
    webpackImage
];

const projects = [
    {
        name: "Simple Todo list application with Vue",
        image: todoImage,
        codeLink: "https://github.com/JohnyKidd/vue-3-practice-todo-list-app",
        siteLink: "https://johnykidd.github.io/vue-3-practice-todo-list-app/",
        tech: ["html", "css", "vue.js"],
        id: 1
    },
    {
        name: "Catmash - facemash clone in PHP and mySQL",
        image: catmashImage,
        codeLink: "https://github.com/JohnyKidd/catmash-facemash-clone-practice-project-",
        tech: ["html", "css", "php", "mariadb"],
        id: 2
    },
    {
        name: "A Star Wars themed fantasy landing page",
        image: swImage,
        codeLink: "https://github.com/JohnyKidd/SW3-3D-fantasy-landing-page",
        siteLink: "https://johnykidd.github.io/SW3-3D-fantasy-landing-page/",
        tech: ["html", "css", "javascript"],
        id: 3
    },
    {
        name: "A simple weather application",
        image: weatherImage,
        codeLink: "https://github.com/JohnyKidd/weatherapp_javascript",
        siteLink: "https://johnykidd.github.io/weatherapp_javascript/s",
        tech: ["html", "css", "javascript"],
        id: 4
    },
    {
        name: "Application for counting calories (In progress)",
        image: nutritioImage,
        codeLink: "https://github.com/JohnyKidd/nutritio",
        siteLink: "https://johnykidd.github.io/nutritio/",
        tech: ["html", "css", "javascript", "REST"],
        id: 5
    },
    {
        name: "A little tic-tac-toe game",
        image: tictactoeImage,
        codeLink: "https://github.com/JohnyKidd/tictactoe_javascript",
        siteLink: "https://johnykidd.github.io/tictactoe_javascript/",
        tech: ["html", "css", "javascript"],
        id: 6
    }
];
</script>

<template>
    <div class="grid-container">
        <a name="home"></a>
        <Greeting />
        <h2>Technologies I work with:</h2>
        <div class="flex-container">
            <SliderTech :technologies="technologies" />
        </div>
        <h2>Tools I can use:</h2>
        <div class="flex-container">
            <SliderTech :technologies="tools" />
        </div>
        <a name="projects"></a>
        <h2>My Projects:</h2>
        <div class="project-grid">
            <Project :projects="projects" />
        </div>
        <a name="contact"></a>
        <Personal />
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