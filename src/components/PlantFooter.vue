<script setup></script>

<template>
    <footer>
        <div class="contact">
            <h2>Vi hörs</h2>
            <address>
                <div>
                    <img src="/svg/phone.svg" alt="Phone" />
                    <span>0701-234567</span>
                </div>
                <div>
                    <span>mail@mail.se</span>
                    <img src="/svg/envelope.svg" alt="Mail" />
                </div>
            </address>
        </div>
        <div class="logo">
            <img src="/svg/logo.svg" alt="The PP logo" />
        </div>
    </footer>
</template>

<style scoped>
footer {
    display: grid;
    @media screen and (min-width: 800px) {
        grid-template: 1fr / 1fr 1fr;
    }
    background: center / cover url("/img/hand.jpg");
    margin-top: 80px;
    color: white;
}

address {
    font-style: normal;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

address div {
    display: grid;
    place-items: center;
    grid-auto-flow: column;
    gap: 1rem;
    margin: 1.2rem;
    @media screen and (min-width: 800px) {
        margin: 3rem;
    }
    font-size: 0.8rem;
    @media screen and (min-width: 800px) {
        font-size: 1.5rem;
    }
}

address div img {
    @media screen and (max-width: 799px) {
        width: 0.8rem;
    }
}

.logo {
    display: grid;
    @media screen and (max-width: 799px) {
        aspect-ratio: 1;
    }
    place-items: center;
    @media screen and (max-width: 799px) {
        order: -1;
    }
}

.logo img {
    height: 256px;
    @media screen and (min-width: 800px) {
        width: 95%;
    }
}

.contact {
    background-color: var(--opa-black);
    aspect-ratio: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

h2 {
    font-size: 2.5rem;
    margin: auto;
    @media screen and (min-width: 800px) {
        height: 512px;
        font-size: 6rem;
    }
    display: grid;
    place-items: center;
    color: white;
}
</style>
