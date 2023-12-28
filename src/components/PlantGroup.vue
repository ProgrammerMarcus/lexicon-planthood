<template>
    <div>
        <img src="@/assets/img/farmer.jpg" alt="A farmer picking fruit" />
        <img src="@/assets/img/watering.jpg" alt="Watering plants" />
        <img src="@/assets/img/vegetables.jpg" alt="A bunch of vegetables" />
        <img src="@/assets/img/ffarmer.jpg" alt="A farmer smiling at the camera" />
    </div>
</template>

<style scoped>
div {
    margin-top: 40px;
    display: grid;
    grid-template: 1fr 1fr / 1fr 1fr;
    gap: 10px;
    background-color: var(--brown);
    padding: 15px;
}

img {
    width: 100%;
    aspect-ratio: 1.5;
    object-fit: cover;
}

@media screen and (min-width: 800px) {
    div {
        margin-top: 80px;
        grid-template: 1fr / repeat(4, 1fr);
        gap: 20px;
        padding: 30px;
    }

    img {
        aspect-ratio: 0.8;
    }
}
</style>
