<template>
    <div>
        <h1>Sumar con Input</h1>
        <div class="num1">
            <label>Numero 1: </label>
            <input 
            type="text"
            name="numero1"
            v-model.number="num1"
        >
        </div>

        <div class="num2">
            <label>Numero 2: </label>
            <input 
            type="text"
            name="numero2"
            v-model.number="num2"
        >
        </div>

        

        <div class="resultado">
            <label>Resultado: </label>
            <input 
            type="text"
            name="resultado"
            v-model.number="resultado"
        >
        </div>
        <button 
            type="button"
            @click.prevent="sumar"
            >Sumar
        </button>
       
    </div>
</template>

<script setup>
import { ref } from 'vue';

const num1 = ref()
const num2 = ref()
const resultado = ref()

function sumar() {
    resultado.value = num1.value + num2.value
}


</script>

<style scoped>

.num1 {
    text-align: center;
    margin-bottom: 1rem;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-weight: bold;
    
}

.num2 {
    text-align: center;
    margin-bottom: 1rem;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-weight: bold;
}

.resultado {
    text-align: center;
    margin-bottom: 2rem;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-weight: bold;
}

button {
    background-color: rgb(182, 147, 212);
    border-radius: 0.5rem;
    padding: 1.5rem;
    padding-block: 1rem;
    text-transform: uppercase;
    font-size: small;
    font-weight: bold;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    display: block; /* Asegura que el botón sea tratado como un elemento de bloque */
    margin: 0 auto; /* Centra el botón horizontalmente */
    cursor: pointer;
    
    
}

input {
    background-color: rgb(250, 218, 223);
    border-radius: 0.5rem;
    padding: 0.5rem;
    padding-block: 0.5rem;
    text-transform: uppercase;
    font-size: small;
    font-weight: bold;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
}

/* no se me ven los style REVISAR */
</style>