<script setup>
import NavBar from "./components/NavBar.vue"
import DatosPersonales from "./components/DatosPersonales.vue"
import Educacion from "./components/Educacion.vue";
import Experiencia from "./components/ExperienciaComponent.vue";
import ProyectosComponent from "./components/ProyectosComponent.vue";
import Habilidades from "./components/HabilidadesComponent.vue";
import InteresesComponent from "./components/InteresesComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
</script>

<template>
  <!--Carga de los componentes-->
  <header>
    <!--Barra de navegación-->
    <NavBar/>
    <!--Componente Datos Personales-->
    <DatosPersonales />
  </header>
  <main>
    <section id="educacion"><h2>Educación</h2><Educacion /></section>
    <section id="experiencia"><h2>Experiencia</h2> <Experiencia/> </section>
    <section id="proyectos"><h2>Proyectos</h2> <ProyectosComponent/> </section>
    <section id="habilidades"><h2>Habilidades</h2> <Habilidades /> </section>
    <section id="intereses"><h2>Intereses</h2><InteresesComponent/> </section>
  </main>
  <footer>
    <FooterComponent />
  </footer>
</template>

<style scoped>
  main section{
    color: #fff;
    text-align: center;
    padding: 2rem 0 2rem 0;
  }

  main section h2{
    color: #5b4ce5;
    font-size: 2rem;
    font-weight: 600;
  }
  
</style>
