<script setup>
function scroller() {
    window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth",
    });
}
</script>

<template>
    <a @click="scroller">Till toppen av sidan</a>
</template>

<style scoped>
a {
    display: grid;
    place-content: center;
    text-decoration: none;
    color: black;
    font-size: 2rem;
    text-align: center;
    width: 100%;
    height: 5rem;
    cursor: pointer;
}
@media screen and (max-width: 799px) {
    a {
        height: 4rem;
        font-size: 0.8rem;
    }
}
a:hover {
    background-color: black;
    color: white;
}
</style>
