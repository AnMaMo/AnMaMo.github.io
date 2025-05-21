<script setup>
import PrimaryButton from './components/PrimaryButton.vue'
import BotonFlecha from './components/BotonFlecha.vue'

const scrollTo = (id) => {
  const el = document.getElementById(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<template>
  <!-- Banner -->
  <div class="div100vh">
    <div id="banner-content">
      <h1 id="title">André Martínez Moreno</h1>
      <h2 id="subtitle">Desarrollador de Software & Técnico de Sistemas</h2>

      <!-- <h2 style="margin-top: 15px; background-color: red;">PORTAFOLIO EN CONSTRUCCIÓN</h2> -->

      <!-- Botonera principal -->
      <div style="display: flex; flex-direction: row; margin-top: 10px;">
<PrimaryButton title="Contactar" div="Contacto" @scrollTo="scrollTo" />
<PrimaryButton title="Ver Proyectos" div="Proyectos" @scrollTo="scrollTo" />
      </div>
    </div>
    <BotonFlecha @scrollTo="scrollTo" />
    
  </div>

  <!-- Div Presentacion -->
  <div class="div100vh" style="background-color: red;" id="presentacion">
    <h1>Presentación</h1>
  </div>

  <!-- Div Proyectos -->
  <div class="div100vh" style="background-color: blue;" id="Proyectos">
    <h1>Proyectos</h1>
  </div>

  <!-- Div Contacto -->
  <div class="div100vh" style="background-color: green;" id="Contacto">
    <h1>Contacto</h1>
  </div>


</template>

<style scoped>
.div100vh {
  height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
}

#banner-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
}

#title {
  height: fit-content;
  text-align: center;
  font-size: 5em;
  vertical-align: top;
  font-family: inter;
  font-weight: bold !important;
}

#subtitle {
  font-size: 1.5em;
  color: #a1a1aa;
  text-align: center;
  vertical-align: top;
  font-family: inter;
  margin-top: 10px;
}
</style>
