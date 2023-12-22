<template>
    <div>
        <img src="@/assets/svg/logo.svg" alt="The PP logo" />
        <img src="@/assets/svg/seedling.svg" alt="A seedling" />
        <img src="@/assets/svg/dig.svg" alt="A digging shovel" />
    </div>
</template>

<style scoped>
div {
    display: grid;
    @media screen and (min-width: 700px) {
        grid-template: 256px 256px / 512px 1fr;
    }
}
img {
    object-fit: none;
    width: 100%;
    height: 100%;
}
img:nth-child(1) {
    background: center / cover url("@/assets/img/succulent.avif");
    grid-row: 2 span;
    @media screen and (max-width: 699px) {
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
    @media screen and (max-width: 699px) {
        padding: 15%;
        object-fit: contain;
    }
}
</style>
