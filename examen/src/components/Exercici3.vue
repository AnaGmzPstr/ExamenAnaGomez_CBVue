<template>
    <h2>Filtrar por nombre</h2>
    <input type="text" v-model="search" placeholder="Buscar...">
    <ul>
        <li v-for="persona in filterpersonas" :key="persona">{{ persona }}</li>
    </ul>
</template>
<script setup>
import { ref, computed } from 'vue';

const search = ref('');
const personas = ref([
    'Ana', 
    'Sarah',
    'Max',
    'Hugo',
    'Gabriela', 
    'Dani',
]);

const filterpersonas = computed(() => {
    return personas.value.filter(persona => persona.toLowerCase().includes(search.value.toLowerCase())
    );
});
</script>