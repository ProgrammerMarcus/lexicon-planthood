<template>
    <div>
        <img src="/svg/logo.svg" alt="The PP logo" />
        <img src="/svg/seedling.svg" alt="A seedling" />
        <img src="/svg/dig.svg" alt="A digging shovel" />
    </div>
</template>

<style scoped>
div {
    display: grid;
    @media screen and (min-width: 800px) {
        grid-template: 256px 256px / 512px 1fr;
    }
}
img {
    object-fit: none;
    width: 100%;
    height: 100%;
}
img:nth-child(1) {
    background: center / cover url("/img/succulent.jpg");
    grid-row: 2 span;
    @media screen and (max-width: 799px) {
        grid-column: 2 span;
    }
}
img:nth-child(2) {
    background-color: var(--brown);
}
img:nth-child(3) {
    background-color: var(--green);
}
img:nth-child(n + 2) {
    @media screen and (max-width: 799px) {
        padding: 15%;
        object-fit: contain;
    }
}
</style>
