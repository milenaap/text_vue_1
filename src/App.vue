<script setup>
import ProjectMile from './components/ProjectMile.vue';
import SumarConInput from './components/SumarConInput.vue';
import { ref } from 'vue';

const esForm1 = ref(true)

const cambiarFormulario = () => {
  console.log('cambia')

  //esForm1.value = false
  esForm1.value = !esForm1.value

}

</script>

<template>

  
  <header>
    <img alt="Mimi logo" class="logo" src="./assets/Logo_cocinita_mimi.png" width="100" height="100" />

  </header>

  <div>
    <button
      @click.prevent="cambiarFormulario"
      >
      Cambiar Proyecto</button>
  </div>

  <ProjectMile 
    v-if="esForm1"
  />

  <SumarConInput 
    v-else
  />


  <main>
   
  </main>
</template>

<style>

header {
  display: flex;
  padding: 2.5rem;
}

h1 {
    text-align: center;
    font-family: Verdana, Geneva, Tahoma, sans-serif;

}



</style>
