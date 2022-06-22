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
    <!-- image here -->
</div>
</template>

<style scoped>
.personal{
    margin-top: 1em;
    text-align: center;
}
.personal article{
    font-size: 15px;
    font-weight: 600;
    line-height: 30px;
    max-width: 400px;
}
@media (min-width: 40em) {
   .personal{
    display: grid;
    /* grid-template-columns: 50% 50%; */
    gap: 1em;
   }
}
.personal img{
    max-width: 250px;
    border: 5px solid black;
    border-radius: 50%;
    
}
h2{
    margin-top: 1em;
    margin-bottom: 1em;
}
</style>