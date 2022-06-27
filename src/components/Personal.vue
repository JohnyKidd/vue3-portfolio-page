<template>
<h2>About Me:</h2>
<div class="personal">
    <article>
        My name is Tibor Enyedi.
        I would like to be a full time web developer and my main interest is 
        full stack web development.
        Nowadays I'm working on understanding the fundamentals on a deep level and I constantly
        try new tools to spice things up a bit because I'm always open to learn.
    </article>
    <!-- <img src="" alt=""> -->
</div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Architects+Daughter&display=swap');
.personal{
    margin-top: 1em;
    text-align: center;
}
.personal article{
    word-spacing: .2em;
    font-size: 20px;
    font-weight: 600;
    line-height: 30px;
    max-width: 400px;
}
/* @media (min-width: 40em) {
   .personal{
    display: grid;
    place-items: center;
    grid-template-columns: repeat(2, 1fr);
   }
} */
.personal img{
    max-width: 500px;
    border: 5px solid black;
    border-radius: 50%;
    background: #808cac;
}
h2{
    margin-top: 1em;
    margin-bottom: 1em;
}
</style>