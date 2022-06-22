<template>
    <div class="header">
        <a href="#home">Home</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
    </div>
</template>

<style scoped>
.header{
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
    width: 100%;
    font-size: 2em;
    border-bottom: 5px solid #000;
    outline: 2.5px solid #41B883;
    background: #000;
    position: sticky;
    top: 0;
}
.header a{
    text-decoration: none;
    color: #41B883;
    transition: transform 100ms ease-in-out;
}
.header a:hover{
    background: #fff;
    transform: scale(1.5);
}
</style>