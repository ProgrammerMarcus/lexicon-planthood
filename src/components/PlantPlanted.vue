<script setup>
import PlantItem from "./PlantItem.vue";
import plants from "@/assets/plants.js";
</script>

<template>
    <main>
        <h2>Dina planterade planteringar</h2>
        <div class="list">
            <PlantItem
                class="item"
                :item="plants[0].item"
                :image="plants[0].image"
                :date="plants[0].date"
                :producer="plants[0].producer"
                visibility="hidden"
                v-for="n in 2" />
        </div>
    </main>
</template>

<style scoped>
main {
    margin-top: 30px;
    display: grid;
    place-items: space-between;
    gap: 0.5rem;

    @media screen and (max-width: 800px) {
        margin: 15px;
    }
}

h2 {
    justify-self: center;
    @media screen and (min-width: 799px) {
        font-size: 2rem;
    }
}

.list {
    display: grid;
    grid-template: 1fr / 1fr 1fr;
    gap: 10px;
    @media (min-width: 799px) {
        grid-template: 1fr / repeat(3, 256px);
        justify-content: space-between;
        gap: 10px;
    }
}
</style>
