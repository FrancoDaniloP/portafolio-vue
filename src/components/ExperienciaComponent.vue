<script setup>
import {ref} from "vue";
const titulo = "Desarrollador Front-End";
const fecha = "Julio 2022 - Septiembre 2024";
import autito from "../assets/autito.svg";
const experiencia = ref([
    {id:1, src: autito, descripcion: "Estuve manejando el sitio web de una empresa de venta de autos, donde estuve estilizando la página y manejando el front."}
])
</script>

<template>
  <div class="card">
    <h2 class="titulo">{{ titulo }}</h2>
    <p class="fecha">{{ fecha }}</p>
    <ul>
        <li v-for="item in experiencia" :key="item.id" class="item">
            <img :src="item.src" alt="icono" width="30" height="30">
            <p>{{ item.descripcion }}</p>
        </li>
    </ul>
  </div>
</template>

<style scoped>
    .card {
        padding: 20px;
        margin-bottom: 40px;
        border: 1px solid #504f4f;
        background-color: rgba(30, 40, 48, 0.76);
        border-radius: 20px;
    }
    .titulo {
        color: #5b4ce5;
        font-size: 27px;
        margin-bottom: 10px;
    }
    .fecha {
        color: #7e7e7e;
        font-size: 14px;
        margin-bottom: 10px;
    }
    ul{
        display: flex;
        flex-direction: column;
        padding-left: 20px;
    }
    .item {
        align-items: center;
        display: flex;
        padding: 1rem;
        gap: 1.5rem;
        color: #d5d5d5;
        font-size: 17px;
        margin-bottom: 5px;
    }
   
</style>