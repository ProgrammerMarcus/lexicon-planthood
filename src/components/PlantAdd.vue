<script setup>
import PlantButton from "./PlantButton.vue";
</script>

<template>
    <section>
        <h2>Lägg till ny plantering:</h2>
        <form>
            <div class="inputs">
                <div class="group">
                    <label for="plant_input"> Planta: </label>
                    <input type="text" id="plant_input" />
                </div>
                <div class="group">
                    <label for="date_input"> Datum: </label>
                    <input type="text" id="date_input" />
                </div>
            </div>
            <PlantButton class="btn" text="LÄGG TILL" />
        </form>
    </section>
</template>

<style scoped>
h2 {
    @media screen and (min-width: 700px) {
        justify-self: start;
        font-size: 2rem;
    }
}
.group {
    display: flex;
    flex-direction: column;
}

section {
    display: grid;
    place-items: center;
    grid-template: 1fr / 1fr;
    max-width: 720px;
    margin: 0 auto;
}

.inputs {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    width: 100%;
    place-content: center;
}

label {
    font-size: 0.9rem;
}

input {
    border: none;
    box-shadow: 2px 2px 4px var(--shadow);
}

form {
    display: grid;
    place-items: center;
    gap: 1.5rem;
    width: 100%;
}
input,
label {
    min-width: 347px;
    max-width: 95%;
    align-self: center;
    margin: 0 auto;
}
</style>
