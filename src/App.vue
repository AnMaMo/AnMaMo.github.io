<script setup>
import NavBar from './components/NavBar.vue'
</script>

<template>
  <!--   <NavBar msg="André " /> -->

  <!-- Banner -->
  <div id="banner">

    <div id="banner-content">
      <h1 id="title">André Martínez Moreno</h1>
      <h2 id="subtitle">Desarrollador de Software & Técnico de Sistemas</h2>

      <h2 style="margin-top: 15px; background-color: red;">PORTAFOLIO EN CONSTRUCCIÓN</h2>

    </div>



  </div>

</template>

<style scoped>
#banner {
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
}

#subtitle {
  font-size: 1.5em;
  color: #666;
  text-align: center;
  vertical-align: top;
  font-family: inter;
}
</style>
