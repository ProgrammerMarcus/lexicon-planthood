<script setup></script>

<template>
    <footer>
        <div class="contact">
            <h2>Vi hörs</h2>
            <address>
                <div>
                    <img src="@/assets/svg/phone.svg" alt="Phone" />
                    <span>0701-234567</span>
                </div>
                <div>
                    <span>mail@mail.se</span>
                    <img src="@/assets/svg/envelope.svg" alt="Mail" />
                </div>
            </address>
        </div>
        <div class="logo">
            <img src="@/assets/svg/Logo.svg" alt="The PP logo" />
        </div>
    </footer>
</template>

<style scoped>
footer {
    display: grid;
    @media screen and (min-width: 700px) {
        grid-template: 1fr / 1fr 1fr;
    }
    background: center / cover url("@/assets/img/hand.avif");
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
    @media screen and (min-width: 700px) {
        margin: 3rem;
    }
    font-size: 0.8rem;
    @media screen and (min-width: 700px) {
        font-size: 1.5rem;
    }

}

address div img {
    @media screen and (max-width: 699px) {
        width: 0.8rem;
    }
    
}

.logo {
    display: grid;
    place-items: center;
    aspect-ratio: 1;
    @media screen and (max-width: 699px) {
        order: -1;
    }
}

.logo img {
    @media screen and (min-width: 700px) {
        height: 256px;
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
    @media screen and (min-width: 700px) {
        height: 512px;
        font-size: 6rem;
    }
    display: grid;
    place-items: center;
    color: white;
}
</style>
