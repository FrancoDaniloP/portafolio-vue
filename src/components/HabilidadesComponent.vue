<script setup>
import {ref} from "vue"
import habilidad1 from "../assets/javascript.svg"
import habilidad2 from "../assets/python.svg"
import habilidad3 from "../assets/java.svg"
import habilidad4 from "../assets/react.svg"
import habilidad5 from "../assets/vue.svg"
import habilidad6 from "../assets/sql.svg"
import habilidad7 from "../assets/html.svg"
import habilidad8 from "../assets/css.svg"
import habilidad9 from "../assets/git.svg"
import habilidad10 from "../assets/github.svg"
import habilidad11 from "../assets/figma.svg"
import habilidad12 from "../assets/tailwind.svg"


const languajes = ref([
    {id:1, src: habilidad1, title: "JavaScript", alt:"Languaje"},
    {id:2, src: habilidad2, title: "Python"},
    {id:3, src: habilidad3, title: "Java"},
    {id:4, src: habilidad4, title: "ReactJS"},
    {id:5, src: habilidad5, title: "VueJS"},
    {id:6, src: habilidad6, title: "MySQL"},
    {id:7, src: habilidad7, title: "HTML"},
    {id:8, src: habilidad8, title: "CSS"},
    {id:9, src: habilidad9, title: "Git"},
    {id:10, src: habilidad10, title: "GitHub"},
    {id:11, src: habilidad11, title: "Figma"},
    {id:12, src: habilidad12, title: "TailwindCSS"},
    

])
</script>

<template>
    <div class="card-container">
        <div class="card" v-for="lenguaje in languajes" :key="lenguaje.id">
            <div class="img-container">
                <img :src="lenguaje.src" class="img-lenguaje">
            </div>
            <div class="title-container">
                <h3 class="title-lenguaje">{{ lenguaje.title }}</h3>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card-container{
    width: 100%;
    height: auto;
    margin-top: 0.7rem;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    flex-wrap: wrap;
    padding: 2rem;
}

.card{
    width: 250px;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0.3rem 1rem;
    border: 1px solid #5b4ce5;
    background-color: rgba(240, 255, 255, 0.064);
    transition: all 300ms ease-in-out;
}

.card:hover{
    transform: scale(1.1);
    background-color: rgba(240, 255, 255, 0.13);
}

.img-lenguaje{
    width: 70px;
    height: 100px;
}

.title-lenguaje{
    color: #fff;
    font-weight: 600;
    font-size: 1.2rem;
}

</style>