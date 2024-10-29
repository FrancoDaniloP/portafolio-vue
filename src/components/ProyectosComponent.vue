<script setup>
import {ref} from "vue";
const buttons = "Ver proyecto"
import img1 from "../assets/image.png"
import img2 from "../assets/imagenpag.png"


const proyectos = ref([
    {id:1, src: img1, titulo: "Pagina de muestra", descripcion: "Esta pagina es una pagina para publicitar productos y poder representar una marca personal", link: "https://graceful-tartufo-3ddb79.netlify.app/"},
    {id:2, src: img2, titulo: "Pagina de noticias", descripcion: "Esta pagina es una pagina de prueba para informarte sobre que está pasando en el mundo, con noticias ficticias. ", link: "https://monumental-lily-6f5c1b.netlify.app"}, 
])
</script>

<template>
    <div class="card-container">
        <div v-for="proyec in proyectos" :key="proyec.id" class="card">
            <div class="img-container">
                <img :src="proyec.src" alt="Imagen de proyecto" class="card-img-top">
            </div>
            <h2 class="proyect-title">{{ proyec.titulo }}</h2>
            <p class="proyect-description">{{ proyec.descripcion }}</p>
            <a :href="proyec.link" class="link-project">{{ buttons }}</a>
        </div>
    </div>
</template>

<style scoped>
    .card-container {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 20px;
        gap: 5rem;
    }

    .card {
        width: 350px;
        height: 450px;
        border: 1px solid #5b4ce5;
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        display: flex;
        flex-direction: column;
        padding: 10px;
        background-color: rgba(8, 8, 8, 0.967);
    }

    .img-container {
        width: 100%;
        height: auto;
    }

    .card-img-top {
        width: 100%;
        height: 200px;
        object-fit: cover;
        background-position: center;
        background-repeat: no-repeat;
        border-radius: 10px;
    }

    .proyect-title {
        font-size: 24px;
        margin: 10px 0;
    }

    .proyect-description {
        font-size: 16px;
        margin: 10px 0;
    }

    .link-project{
        background-color: #5b4ce5;
        color: #fff;
        padding: 10px 20px;
        border-radius: 25px;
        text-decoration: none;
        margin: 10px 0;
        width: 150px;
        margin: auto;
        transition: all 0.3s ease-in-out; 
    }

    .link-project:hover{
        background-color: #3b2faa;
    }
</style>