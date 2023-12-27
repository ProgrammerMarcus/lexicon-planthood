<script setup>
import PlantRemove from "./PlantRemove.vue";

defineProps({
    image: String,
    item: String,
    date: String,
    producer: String,
});
</script>

<template>
    <section>
        <img src="@/assets/svg/plant.svg" :alt="item" />
        <div>
            <h3>{{ item }}</h3>
            <span class="date">{{ date }}</span>
            <span class="producer">{{ producer }}</span>
            <PlantRemove class="remove" />
        </div>
    </section>
</template>

<style scoped>
section {
    width: 100%;
    box-shadow: 3px 3px 3px var(--shadow);
    @media screen and (max-width: 699px) {
        font-size: 0.8rem;
    }
}
div {
    display: grid;
    grid-template: 1fr / max-content auto;
    @media screen and (min-width: 700px) {
        grid-template: 2.5rem 2.5rem / 1fr 1fr;
    }
    justify-content: space-between;
    align-items: center;
    margin: 0 5%;
    padding: 0.5rem 0;
    gap: 0.3rem;
}
h3 {
    margin: 0;
    font-size: 1.25em;
    font-weight: 600;
}
img {
    background: center / cover v-bind("`url('${image}')`");
    width: 100%;
    aspect-ratio: 1;
    box-sizing: border-box;
    padding: 15%;
}
.date {
    @media screen and (max-width: 699px) {
        max-width: 4rem;
        font-size: 0.7em;
    }
}
.producer {
    font-size: 0.9em;
}
.date {
    font-weight: bold;
}
.remove,
.date {
    margin: auto 0 auto auto;
}
</style>
