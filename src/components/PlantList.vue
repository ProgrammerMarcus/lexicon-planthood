<script setup>
import PlantItem from "./PlantItem.vue";
import Plants from "@/assets/plants.js"
console.log(Plants.plants)
import { ref } from "vue";
const plants = ref();
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
    </main>
</template>

<style scoped>
.grid {
    display: grid;
}
</style>
