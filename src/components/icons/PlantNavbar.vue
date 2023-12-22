<script setup>
import { ref } from "vue";
const dropdown = ref(window.innerWidth > 700);
addEventListener("resize", (event) => {
    dropdown.value = window.innerWidth > 700;
});
</script>
<template>
    <nav>
        <img
            @click="dropdown = !dropdown"
            id="burgir"
            src="@/assets/svg/burgir.svg"
            alt="A burgir (not to be confused with burger)" />
        <div v-show="dropdown" id="links" class="links">
            <a href="" id="link_planer">PLANER</a>
            <a href="" id="link_history">HISTORIK</a>
            <a href="" id="link_tips">TIPS</a>
            <a href="" id="link_login">LOGGA IN</a>
        </div>
    </nav>
</template>

<style scoped>
#burgir {
    position: absolute;
    top: 0.5rem;
    right: 0.5rem;
    height: 2.5rem;
}

.links {
    display: grid;
}
a {
    color: var(--green);
    text-decoration: none;
    font-weight: bold;
    text-align: center;
    padding: 1.2rem;
}
a:hover {
    background-color: var(--green);
    color: white;
}
@media screen and (max-width: 699px) {
    .links {
        place-items: center;
        position: absolute;
        top: 3.5rem;
        right: 0.5rem;
        z-index: 999;
        background-color: white;
        border-radius: 9px;
        box-shadow: 0px 5px 5px var(--shadow);
    }
}
@media screen and (min-width: 700px) {
    .links {
        grid-auto-flow: column;
        box-shadow: 0px 5px 5px var(--shadow);
    }

    #burgir {
        display: none;
    }
}
</style>
