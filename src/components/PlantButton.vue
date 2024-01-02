<script setup>
defineProps({
    text: String,
});
</script>

<template>
    <a href="">{{ text }}</a>
</template>

<style scoped>
a {
    background-color: var(--green);
    text-decoration: none;
    color: white;
    border-radius: 9px;
    padding: 0.9rem 1.5rem;
    font-weight: bold;
    font-size: 1.2rem;
    box-shadow: 0 5px 10px var(--shadow);
    @media screen and (max-width: 799px) {
        font-size: 1rem;
    }
}

a:hover {
    background-color: black;
}

</style>
