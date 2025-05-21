<!-- Scripts -->
<script setup>
import { ref } from 'vue'

defineProps({
    title: String,
    div: String
})

const count = ref(0)
</script>

<template>

<!-- Boton principal -->
<button @click="$emit('scrollTo', div)" style="margin-top: 15px;">
    {{ title }}
</button>

</template>

<style scoped>
button {
    border: 1px solid white;
    background-color: transparent;
    color: white;
    padding: 15px;
    font-size: 1.3rem;
    margin: 20px;
    cursor: pointer;
}

/** El hover sera un gradiente en blanco a transparente con una animacion de 1 segundo */
button:hover {
    background: white;
    color: black;
    transition: background 0.4s;
}

</style>
