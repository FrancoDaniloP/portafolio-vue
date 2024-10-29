<script setup>
const nombre = "Danilo Pietropaolo"
const titulo = "Técnico Universitario en Programación"


</script>

<template>
<section class="datos-personales">
    <div class="card">
        <h1>{{ nombre }}</h1>
        <div class="container-img">
            <img src="../assets/perfil.jpg" alt="Foto de perfil" class="img-danilo">
        </div>
        <p>Hola, Bienvenido a mi portafolio de proyectos. Soy un {{ titulo }} sin experencia todavia, en el desarrollo de apps webs y móviles</p>
        
    </div>

</section>
</template>

<style scoped>
.datos-personales{
    color: #fff;
    margin-top: 5rem;
    margin-bottom: 5rem;
}

.card{
    padding: 8px;
    text-align: center;
}

.card h1{
    font-size: 37px;
    margin-bottom: 1rem;
}
.card p{
    font-size: 18px;
}

.container-img{
    width: 200px;
    height: auto;
    margin: 0 auto;
    margin-bottom: 2rem;
}
.img-danilo{
    width: 200px;
    border-radius: 100px;
    border: 3px solid #5b4ce5;
    margin: 0 auto;
}

</style>