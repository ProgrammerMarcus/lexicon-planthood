<script setup>
import PlantHome from "./components/PlantHome.vue";
import PlantPlans from "./components/PlantPlans.vue";
import { ref, computed } from "vue";
const routes = {
    "/": PlantHome,
    "/plans": PlantPlans,
};

const currentPath = ref(window.location.hash);

window.addEventListener("hashchange", () => {
    currentPath.value = window.location.hash;
});

const currentView = computed(() => {
    return routes[currentPath.value.slice(1) || "/"] || NotFound;
});
</script>

<template>
    <component :is="currentView" />
</template>

<style scoped></style>
