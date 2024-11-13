<template>
    <header class="p-5 mb-2 mt-4 text-center rounded-4 bg-vue-dark text-white cabecalho">
        <h1 class="header-title">Calculator VueJS</h1>
        <p class="header-subtitle">Simplicity in everyday use.</p>
    </header>
</template>

<script setup>
</script>

<style scoped>
.cabecalho{
    max-width: 400px;
    margin: auto;
    border-radius: 10px;
}

.bg-vue-dark {
    background: #030322;
    color: #fff;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.4);
    border-radius: 12px;
}

.header-title{
    font-size: 2.5rem;
    font-weight: 700;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    margin: 0;
    padding: 0;
    animation: fadeIn 1s ease-in-out;
}

.header-subtitle{
    font-size: 1.2rem;
    font-weight: 300;
    opacity: 0.8;
    margin: 0;
}

@keyframes fadeIn {
from {
        opacity: 0;
        transform: translateY(-10px);
    }
    to {
    opacity: 1.5;
    transform: translateY(0);
    }
}

@media screen and (max-width: 768px) {
    .header-title {
        font-size: 2rem;
    }

    .header-subtitle {
        font-size: 1rem;
    }

    .p-5 {
        padding: 2rem;
    }
}
</style>
