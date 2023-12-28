<script setup>
import PlantAdd from "./PlantAdd.vue";
import PlantGroup from "./PlantGroup.vue";
import PlantMy from "./PlantMy.vue";
import PlantNavbar from "./PlantNavbar.vue";
import PlantPlanned from "./PlantPlanned.vue";
import PlantPlanted from "./PlantPlanted.vue";
import PlantReturn from "./PlantReturn.vue";
</script>

<template>
    <PlantNavbar />
    <PlantMy />
    <div class="limiter">
        <PlantAdd />
        <PlantPlanned />
        <PlantPlanted />
    </div>
    <PlantGroup />
    <PlantReturn />
</template>

<style scoped>
  .limiter {
    max-width: 720px;
    margin: 0 auto;
  }
</style>
