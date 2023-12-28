<script setup>
import PlantButton from "./PlantButton.vue";
</script>

<template>
    <header>
        <h1>PLANNED PLANTHOOD</h1>
        <div>
            <h2>Säsong att så</h2>
            <p>
                Våren är äntligen här i kollektivet! Lorem ipsum dolor sit amet consectetur. Sit
                venenatis arcu nunc consectetur neque. Vel amet netus amet eu elit.
            </p>
            <PlantButton text="SÅ-TIPS" />
        </div>
        <img src="@/assets/svg/Vectorseedpackage.svg" alt="A seed package" />
        <hr />
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
    @media screen and (max-width: 799px) {
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
    margin: 0 10px;
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

@media screen and (min-width: 800px) {
    header {
        grid-template: max-content 1fr / auto auto;
        margin: 0 5%;

        h1 {
            grid-column: 2 span;
            order: -2;
        }

        img {
            grid-row: 2 span;
            order: -1;
            justify-self: end;
            padding: 40px;
            margin-right: 20px;
            height: 280px;
        }

        div {
            display: grid;
            max-width: 512px;
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
