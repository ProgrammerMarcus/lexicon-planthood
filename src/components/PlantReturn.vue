<template>
    <a href="#root">Till toppen av sidan</a>
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
    }
    @media screen and (max-width: 699px) {
        a {
            height: 4rem;
            font-size: 0.8rem;
        }
    }
</style>
