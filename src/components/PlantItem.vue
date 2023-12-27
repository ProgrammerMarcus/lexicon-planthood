<script setup>
import PlantRemove from './PlantRemove.vue';

defineProps({
  image: String,
  item: String,
  date: String,
  producer: String,
})
</script>

<template>
    <section>
        <img src="@/assets/svg/plant.svg" :alt="item">
        <div>
            <h3>{{ item }}</h3>
            <span class="date">{{ date }}</span>
            <span class="producer">{{ producer }}</span>
            <PlantRemove class="remove"/>
        </div>
    </section>
</template>

<style scoped>
    section {
        width: 256px;
        box-shadow: 3px 3px 3px var(--shadow);
    }
    div {
        display: grid;
        grid-template: 1fr 1fr / 1fr 1fr;
        justify-content: space-between;
        align-items: center;
        margin: 0 5%;
        height: 6rem;
        padding-bottom: 0.5rem;
    }
    h3 {
        margin: 0;
        font-size: 1.5rem;
        font-weight: normal;
    }
    img {
        background: center / cover v-bind(image);
        width: 100%;
        aspect-ratio: 1;
        box-sizing: border-box;
        padding: 15%;
    }
    .producer {
        font-size: 0.9em;
    }
    .date {
        font-weight: bold;
    }
    .remove, .date {
        margin: auto 0 auto auto;
    }
</style>
