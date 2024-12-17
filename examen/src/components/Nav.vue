<template>
    <nav>
        <ul>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="exercici1">Exercici 1: Llista de productes</RouterLink>
            <RouterLink to="exercici2">Exercici 2: Comptador</RouterLink>
            <RouterLink to="exercici3">Exercici 3: Usuaris</RouterLink>
        </ul>
    </nav>
</template>

<script setup>
import { RouterLink } from 'vue-router';
</script>