<script setup>
import { ref } from 'vue';
const derechos = "© 2021 - Portafolio de Desarrollo Web";
const nombre = "Danilo Pietropaolo";
import red1 from "../assets/linkedin.svg";
import red2 from "../assets/instagram.svg";
import red3 from "../assets/github.svg";
import red4 from "../assets/curriculum.svg";


const redes = [
    {id: 1, name: "LinkedIn", src: red1, url: "https://www.linkedin.com/in/danilo-pietropaolo-251214261/"},
    {id: 2, name: "Instagram", src: red2, url: "https://www.instagram.com/danilo_pietro0/"},
    {id: 3, name: "GitHub", src: red3, url: "https://github.com/FrancoDaniloP"},
    {id: 4, name: "Curriculum", src: red4, url: ""}
]
const telefono = "+54 2634 556 966"
const residencia = "La Paz, Mendoza, Argentina"
</script>

<template >
    <footer>
        <p>{{ derechos }}</p>
        <h3>📞 Mi teléfono personal: <span>{{ telefono }}</span></h3>
        <h4>📍 {{ residencia }}</h4>
        <h4 class="redes">Redes Sociales:</h4>
        <ul class="container-lista">
            <li v-for="red in redes" :key="red.id">
                <a :href="red.url"><img class="icon-redsocial" :src="red.src" :alt="red.name" width="35rem"></a>
            </li>
        </ul>
    </footer>
</template>

<style scoped>
    footer{
        width: 100%;
        margin-top: 5rem;
        border-top: 2px solid #525252;
        border-right: 2px solid #525252;
        border-left: 2px solid #525252;
        color: #838282;
        font-size: 1.1rem;
        text-align: center;
        padding: 2rem;
}
    .container-lista{
    display: flex;
    flex-direction: row;
    gap: 5rem;
    justify-content: center;
    margin: 1rem 0 0 0;
}
.footer h3{
    font-size: 18px;
}

.footer h3 span{
    color: #5b4ce5;
}

.redes{
    color: #5b4ce5;
}

.footer h4{
    font-size: 17px;
}
</style>