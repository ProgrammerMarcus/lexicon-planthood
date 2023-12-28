<script setup>
import PlantButton from "./PlantButton.vue";
import PlantItem from "./PlantItem.vue";
import plants from "@/assets/plants.js";
</script>

<template>
    <main>
        <h2>Våra planerade planteringar:</h2>
        <div class="grid">
            <PlantItem
                v-for="plant in plants"
                :item="plant.item"
                :image="plant.image"
                :date="plant.date"
                :producer="plant.producer" />
        </div>
        <PlantButton class="more" text="Visa fler" />
    </main>
</template>

<style scoped>
h2,
.more {
    display: grid;
    place-content: center;
    width: max-content;
    margin: 2rem auto 2rem auto;
}
.grid {
    display: grid;
    grid-template: 1fr / repeat(2, 45%);
    justify-content: center;
    gap: 10px;
    @media (min-width: 800px) {
        grid-template: 1fr / repeat(3, 256px);
        gap: 30px;
    }
    place-items: center;
}
</style>
