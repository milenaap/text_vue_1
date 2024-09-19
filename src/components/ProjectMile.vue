<template>
    <div>
        <h1>Project Mile</h1>

        
        <p>El resultado es: {{ resultado }}</p>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const num1 = ref(0)
const num2 = ref(0)
const resultado = ref(0)

num1.value = 1250
num2.value = 1750

resultado.value = num1.value + num2.value

</script>

<style scoped>



</style>