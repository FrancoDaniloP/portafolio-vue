<template>
    <nav class="navbar">
      <div class="navbar-menu">
        <ul>
          <a v-for="nav in navegacion" :key="nav.nombre" :href="nav.enlace" class="nav-item">{{ nav.nombre }}</a>
        </ul>
      </div>
    </nav>
</template>

<script setup>
import { ref } from 'vue'
const navegacion = ref([
    {id:1, nombre: "Sobre Mi", enlace:"#sobre-mi"},
    {id:2, nombre: "Educacion", enlace:"#educacion"},
    {id:3, nombre: "Experiencia", enlace:"#experiencia"},
    {id:4, nombre: "Proyectos", enlace:"#proyectos"},
    {id:5, nombre: "Habilidades", enlace:"#habilidades"},
])
</script>

<style scoped>
.navbar{
  background-color: #5b4ce5;
  color: #fff;
  padding: 0.5rem 1rem;
  align-items: center;
  border-radius: 25px;
}

.navbar-item{
  color: #fff;
  text-decoration: none;
  margin-right: 1rem;
}

.navbar-menu{
  display: flex;
  justify-content: center;
}

.navbar-menu ul{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 1.5rem;
}


.nav-item{
  color: #fff;
  font-size: 15px;
  text-decoration: none;
  transition: all 0.3s ease-in-out;
  padding: 3.5px;
  font-weight: 600;
}

.nav-item:hover{
  color: #000
}


</style>