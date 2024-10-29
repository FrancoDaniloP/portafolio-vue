<script setup>
import {ref} from 'vue';
const intereses = ref([
    "Programar en React, utilizando Hooks y funcionalidades",
    "Aprender nuevas tecnologías, como Vue.js, Angular, terminar de perfeccionar MySQL, etc",
    "Ir al gimnasio, entrenar",
    "Leer, ya sea documentación o libros sobre tecnología",
    "Jugar videojuegos, como Valorant, Counter Strike GO, etc",
]);
</script>

<template>
    <div class="intereses_container">
        <ul class="list_intereses">
            <li v-for="interes in intereses" :key="interes">
                {{interes}}
            </li>
        </ul>
    </div>
    
</template>

<style scoped>
.intereses_container{
    width: 100%;
    border: 2px solid #5b4ce5;
    color: #fff;
}
.list_intereses{
    list-style: none;
    display: flex;
    flex-direction: column;
    align-items: start;
    gap: 0.7rem;
    padding: 1.5rem;
}
.list_intereses li{
    color: #fff;
    font-size: 1.1rem;
    font-weight: 500;
}
</style>