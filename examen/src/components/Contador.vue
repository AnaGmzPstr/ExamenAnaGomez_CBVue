<template>
    <div style="width: 200px;">
        <button
        @click="incrementar">
            +1
        </button>
        <button
        @click="decrementar">
            -1
        </button>
    </div>
</template>

<script setup>
import { inject } from 'vue';

const contador = inject('contador');
const incrementar = inject('incrementar');
const decrementar = inject('decrementar');

</script>