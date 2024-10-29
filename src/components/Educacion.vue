<script setup>
const languages = [
    {id: 1, title: "DESARROLLO WEB", name: "HTML5 Y CSS", description: "Aprendí primeramente HTML y luego CSS, desde Udemy y YouTube, siguiendo a creadores de contenido de programación. Creando proyectos y diseños webs fabulosos."},
    {id: 2, title: "JavaScript", name: "JavaScript Moderno", description: "Conocimientos en JavaScript, aprendiendo desde cero, con cursos de Udemy y YouTube, siguiendo a creadores de contenido de programación. Creando proyectos y aprendiendo la funcionalidad del sitio web."},
    {id: 3, title: "React", name: "Framework de JavaScript", description: "Aprendiendo React, con sus hooks, componentes y manera mas dinámica de trabajar y realizar sitios webs y aplicaciones."},
    {id: 4, title: "Python", name: "Lenguaje de Programación", description: "Aprendiendo Python, con sus librerías y funcionalidades, para realizar aplicaciones y proyectos de programación."},
    {id: 5, title: "Java", name: "Lenguaje de Programación", description: "Aprendiendo Java, desde la UTN de San Rafael, un lenguaje de programación increíble, que usa mucho la POO(Programacion Orientada a Objetos)"},
    {id: 6, title: "NodeJS", name: "Backend", description: "Un entorno de ejecución de JavaScript que sirve para varias cosas en la programación. Por ejemplo: el backend"},
    {id: 7, title: "MySQL", name: "Base de Datos", description: "Aprendiendo MySQL, un sistema de gestión de bases de datos relacional, que se usa mucho en la programación para el almacenamiento de datos."}
]
</script>

<template>
    <div class="timeline">
        <ul>
          
            <li v-for="lang in languages" :key="lang.id">
                <div class="content">
                    <h3>{{ lang.title }}</h3>
                    <h4>{{ lang.name }}</h4>
                    <p>{{ lang.description }}</p>
                </div>
            </li>
          <div style="clear: both"></div>
        </ul>
      </div>
      
</template>

<style scoped>
.timeline{
        margin-top: 40px;
        margin-bottom: 40px;
        position: relative;
    }
    .timeline:before{
        content: '';
        position: absolute;
        left: 50%;
        width: 2px;
        height: 100%;
        background: #6658ea
    }
    .content{ border: #6658ea 1px solid; padding: 20px; border-radius: 20px; color: rgb(212, 214, 220);}
    .timeline ul{ margin: 0; padding: 0}
    .timeline ul li{ 
        list-style: none;
        position: relative;
        width: 50%;
        padding: 20px 40px;
        box-sizing: border-box;
    }
    
    .timeline ul li:nth-child(odd){
        float: left;
        text-align: right;
        clear: both;
    }
    .timeline ul li:nth-child(odd)::before{
        content: '';
        position: absolute;
        top: 40px;
        right: -14px;
        width: 20px;
        height: 20px;
        background: white;
        border: 2px solid #6658ea;
        border-radius: 50%
    }
    .timeline ul li:nth-child(odd)::after{
        content: '';
        position: absolute;
        border-style: solid;
        width: 0;
        height: 0;
        top: 44px;
        right: 25px;
        border-width: 10px 0 10px 15px;
        border-color: transparent transparent transparent #6658ea;
    }

    .timeline ul li:nth-child(even){
        float: right;
        text-align: left;
        clear: both;
    }
   
   
    .timeline ul li:nth-child(even)::before{
        content: '';
        position: absolute;
        top: 40px;
        left: -10px;
        width: 20px;
        height: 20px;
        background: white;
        border: 2px solid #6658ea;
        border-radius: 50%
    }
    .timeline ul li:nth-child(even)::after{
        content: '';
        position: absolute;
        border-style: solid;
        width: 0;
        height: 0;
        top: 44px;
        left: 25px;
        border-width: 10px 15px 10px 0px;
        border-color: transparent #6658ea transparent transparent;
    }
    @media all and (max-width: 768px) {
        .timeline:before{
            left: 0%;
        }
        .timeline ul li{ 
            width: 100%;
        }
        .timeline ul li:nth-child(odd){
            float: right;
            text-align: left;
        }
        .timeline ul li:nth-child(odd)::before{
            left: -10px;
        }
        .timeline ul li:nth-child(odd)::after{
            left: 25px;
            border-width: 10px 15px 10px 0px;
            border-color: transparent #6658ea transparent transparent;
        }
        
    }
</style>