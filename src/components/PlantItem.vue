<script setup>
import PlantRemove from "./PlantRemove.vue";

defineProps({
    image: String,
    item: String,
    date: String,
    producer: String,
    visibility: {
        type: String,
        default: "visible",
    },
});
</script>

<template>
    <section>
        <div class="bg">
            <img class="hide" src="@/assets/svg/plant.svg" :alt="item" />
        </div>
        <div class="order">
            <h3>{{ item }}</h3>
            <span class="date">{{ date }}</span>
            <span class="producer">{{ producer }}</span>
            <PlantRemove class="remove" />
        </div>
    </section>
</template>

<style scoped>
.bg {
    background: center / cover v-bind("`url('${image}')`");
    margin: 0;
    aspect-ratio: 1;
    min-height: 155px;
    display: grid;
    place-items: center;
    place-content: center;
    width: 100%;
}

section {
    width: 100%;
    box-shadow: 3px 3px 3px var(--shadow);
    @media screen and (max-width: 799px) {
        font-size: 0.8rem;
    }
}
.order {
    display: grid;
    grid-template: 1fr / max-content auto;
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
    width: 60%;
    @media screen and (min-width: 800px) {
        width: 100%;
    }
}
.date {
    @media screen and (max-width: 799px) {
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

.hide {
    @media screen and (max-width: 800px) {
        visibility: v-bind(visibility);
    }
}
</style>
