<template>
    <ul>
        <RouterLink :to="{name:'productDetail', params:{producteId:producte.id, producteNom:producte.nom, producteDes: producte.descripcio}}" 
        v-for="producte in dataProductes" :key="producte.id"
        :nom="producte.nom" :desc="producte.descripcio"
        >
            {{ producte.nom }}
        </RouterLink>
    </ul>
    <RouterView/>

</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router';
import { useRoute } from 'vue-router';
import { provide } from 'vue';
const route = useRoute();

const dataProductes=[
    {
        id:1,
        nom:"Producte 1",
        descripcio: "Descripció producte 1",
    },
    {
        id:2,
        nom:"Producte 2",
        descripcio: "Descripció producte 2",
    },
    {
        id:3,
        nom:"Producte 3",
        descripcio: "Descripció producte 3",
    },
];



</script>