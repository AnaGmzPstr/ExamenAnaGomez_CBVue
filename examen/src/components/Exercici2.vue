<template>
<p>Contador padre: {{ contador }}</p>
<Contador/>
</template>

<script setup>
import Contador from '@/components/Contador.vue';
import { ref, provide} from 'vue';
// Variable reactiva
const contador = ref(0);
// Proveer el contador
provide('contador', contador);
// Proveer funciones que incrementan y decrementan
provide('incrementar', () => {
    contador.value++;
});
provide('decrementar', () =>{
    contador.value--;
})
</script>