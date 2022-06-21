<template>
<div class="contact-flex">
    <a href="mailto:enyedi.tibor1996@gmail.com" target="#">Email me!</a>
    <a href="https://github.com/JohnyKidd" target="#">Check my Github profile!</a>
</div>
</template>

<style scoped>
a{
    text-decoration: none;
    color: #000;
    font-weight: 900;
    position: relative;
}
a::after{
    content: '';
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 2px;
    background: currentColor;
    transform: scaleX(0);
    transform-origin: right;
    transition: transform 250ms ease-in;
}
a:hover::after{
    transform: scaleX(1);
    transform-origin: left;
}
.contact-flex{
    display: flex;
    margin-top: 5em;
    padding: 1em;
    gap: 5em;
    width: 100%;
    justify-content: center;
    background: #41B883;
    font-size: 20px;
    text-align: center;
}
</style>