<script setup>
import Greeting from './components/Greeting.vue';
import SliderTech from './components/SliderTech.vue';
import Project from './components/Project.vue';
import Contact from './components/Contact.vue';
import Personal from './components/Personal.vue';

const technologies = [
    "../public/imgs/html.svg",
    "../public/imgs/css.svg",
    "../public/imgs/js.svg",
    "../public/imgs/mysql.svg",
    "../public/imgs/php.svg",
    "../public/imgs/vue.svg",
];

const tools = [
    "../public/tools/photoshop.svg",
    "../public/tools/github.svg",
    "../public/tools/tailwind.svg",
    "../public/tools/vite.svg",
    "../public/tools/vscode.svg",
    "../public/tools/webpack.svg",
];

const projects = [
    {
        name: "Simple Todo list application with Vue",
        image: "../public/projects/todo.png",
        codeLink: "https://github.com/JohnyKidd/vue-3-practice-todo-list-app",
        siteLink: "https://johnykidd.github.io/vue-3-practice-todo-list-app/",
        tech: ["html", "css", "vue.js"],
        id: 1
    },
    {
        name: "Catmash - facemash clone in PHP and mySQL",
        image: "../public/projects/catmash.png",
        codeLink: "https://github.com/JohnyKidd/catmash-facemash-clone-practice-project-",
        tech: ["html", "css", "php", "mariadb"],
        id: 2
    },
    {
        name: "A Star Wars themed fantasy landing page",
        image: "../public/projects/swlanding.png",
        codeLink: "https://github.com/JohnyKidd/SW3-3D-fantasy-landing-page",
        siteLink: "https://johnykidd.github.io/SW3-3D-fantasy-landing-page/",
        tech: ["html", "css", "javascript"],
        id: 3
    },
    {
        name: "A simple weather application",
        image: "../public/projects/weather.png",
        codeLink: "https://github.com/JohnyKidd/weatherapp_javascript",
        siteLink: "https://johnykidd.github.io/weatherapp_javascript/s",
        tech: ["html", "css", "javascript"],
        id: 4
    },
    {
        name: "Application for counting calories (In progress)",
        image: "../public/projects/nutritio.png",
        codeLink: "https://github.com/JohnyKidd/nutritio",
        siteLink: "https://johnykidd.github.io/nutritio/",
        tech: ["html", "css", "javascript", "REST"],
        id: 5
    },
    {
        name: "A little tic-tac-toe game",
        image: "../public/projects/tictactoe.png",
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