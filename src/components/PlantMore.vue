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
    object-fit: scale-down;
    box-sizing: content-box;
    width: max-content;
    height: 280px;
}

h1 {
    color: var(--green);
    font-weight: normal;
    margin-top: 30px;
    @media screen and (max-width: 699px) {
        font-size: 1.6rem;
    }
}

h2 {
    margin-bottom: 0;
    font-weight: bold;
}

div {
    display: grid;
    place-items: center;
    text-align: center;
    grid-row: 2 span;
}

header {
    display: grid;
    place-items: center;
}

hr {
    margin-top: 7%;
    height: 3px;
    width: 300px;
    background-color: var(--green);
}

@media screen and (min-width: 700px) {
    header {
        grid-template: min-content auto / auto auto;
        margin: 0 5%;

        img {
            grid-row: 2 span;
            order: 1;
            justify-self: start;
            padding: 40px;
            margin-left: 20px;
            height: 280px;
        }

        div {
            display: grid;
            max-width: 512px;
            justify-self: end;
            margin-left: 20px;
            text-align: left;
            grid-row: 2 span;
        }

        h2 {
            margin: 0 auto 0 0;
        }
        a {
            margin: 0 auto 0 0;
        }

        hr {
            grid-column: 2 span;
        }
    }
}
</style>
