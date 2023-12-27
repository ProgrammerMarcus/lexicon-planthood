<script setup>
import PlantButton from "./PlantButton.vue";
</script>

<template>
    <header>
        <img src="@/assets/svg/plant.svg" alt="A seed package" />
        <div>
            <h2>Våra tidigare odlingar</h2>
            <p>
                Våren är äntligen här i kollektivet! Lorem ipsum dolor sit amet consectetur. Sit
                venenatis arcu nunc consectetur neque. Vel amet netus amet eu elit.
            </p>
            <PlantButton text="Planterade plantor" />
        </div>
    </header>
</template>

<style scoped>
img {
    background-color: var(--green);
    border-radius: 100%;
    aspect-ratio: 1;
    padding: 5%;
    object-fit: contain;
    margin-top: 20px;
}

h2 {
    margin-bottom: 0;
    font-weight: bold;
}

div {
    display: grid;
    place-items: center;
    text-align: center;
    margin: 0 10px;
}

header {
    display: grid;
    place-items: center;
}

@media screen and (min-width: 700px) {
    header {
        grid-template: auto 1fr / 1fr 1fr;
        margin: 0 5%;

        h1 {
            grid-column: 2 span;
            order: -2;
        }

        img {
            grid-row: 2 span;
            order: -1;
            justify-self: end;
            padding: 10%;
            margin-right: 20px;
        }

        div {
            display: grid;
            width: 512px;
            justify-self: start;
            margin-left: 20px;
            text-align: left;
        }

        h2 {
            margin: 0 auto 0 0;
        }

        a {
            margin: 0 0 0 auto;
        }

        hr {
            grid-column: 2 span;
        }
    }
}
</style>
