<template>
    <button aria-label="Ta bort">
        <img src="/svg/trash.svg" alt="Ta bort" />
    </button>
</template>

<style scoped>
button {
    background: none;
    border: none;
    cursor: pointer;
}

@media (min-width: 800px) {
    button:after {
        content: "TA BORT";
    }
    button {
        background-color: var(--red);
        color: white;
        font-weight: bold;
        padding: 0.5rem 1rem;
        font-size: 0.9rem;
        border-radius: 9px;
    }
    button img {
        display: none;
    }
    button:hover {
    background-color: black;
}
}

</style>
