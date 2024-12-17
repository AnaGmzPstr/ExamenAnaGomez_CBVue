<template>
    <h2>Detall del producte</h2>
    <h4>Id: {{ props.id }}</h4>
    <p>Nom: {{ props.nom }} </p>
    <p>Descripció: {{ props.descripcio }} </p>
</template>

<script setup>
import { useRoute } from 'vue-router';
import { inject } from 'vue';
const route = useRoute();

const props = defineProps({
    id:{
        type: Number,
    },
/*     nom:{
        type: String,
    },
    desc:{
        type: String,
    } */
});


</script>