<script setup>
import Header from './components/Header.vue'
import Preparatation from './components/Preparatation.vue'
import Ingredients from './components/Ingredients.vue'
import Instructions from './components/Instructions.vue'
import Nutrition from './components/Nutrition.vue'
import './assets/global.css';

</script>

<template>
  <div class="app-container">
    <Header />
    <preparatation />
    <Ingredients />
    <Instructions />
    <Nutrition />
  </div>
</template>

<style scoped>
/* Importa las fuentes desde Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Open+Sans:wght@400;600&display=swap');




/* Fondo del contenedor principal */
.app-container {
  background-color: #ffffff;
  padding: 20px;
  max-width: 800px;
  margin: 0 auto;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  /* Bordes redondeados para dar un aspecto más moderno */
}

/* Estilo del título principal */
h1,
h2 {
  font-family: 'Merriweather', serif;
  /* Fuente para títulos */
  color: #723e55;
  /* Color de los encabezados */
  font-weight: 700;
  margin-bottom: 10px;
}

/* Estilo de las secciones de subtítulos */
h3 {
  font-family: 'Merriweather', serif;
  color: #723e55;
  font-weight: 700;
  margin-top: 20px;
  margin-bottom: 10px;
}

/* Estilo de los textos de párrafos */
p {
  font-family: 'Open Sans', sans-serif;
  /* Fuente del cuerpo de texto */
  color: #333;
  line-height: 1.6;
  margin-bottom: 15px;
}

/* Estilo de las listas (como los ingredientes e instrucciones) */
ul,
ol {
  font-family: 'Open Sans', sans-serif;
  color: #333;
  margin-bottom: 15px;
  padding-left: 20px;
}

li {
  margin-bottom: 10px;
  line-height: 1.6;
}

/* Estilo para resaltar títulos dentro de listas */
li strong {
  font-family: 'Merriweather', serif;
  /* Resaltar títulos dentro de la lista */
  color: #723e55;
  font-weight: 700;
}
</style>
