<script setup>
import About_me from './About_me.vue';
import Skills from './Skills.vue';
import Portafolio from './Portafolio.vue';
import Contacto from './Contacto.vue';
</script>

<template>
    <section class="inicio" id="inicio">
            <div class="contenedor-img">
                <img src="../assets/fondo1.jpg" alt="">
            </div>
            <div class="texto ">
                <h1>Manuel Rodas</h1>
                <h2>Estudiante de Ingenieria en Ciencias de la Computacion</h2>
                <div class="redes">

                </div>
            </div>
    </section>
    <section class="sobremi">
        <About_me/>
    </section>
    <section class="skills">
        <Skills/>
    </section>
    <section class="portafolio">
        <Portafolio/>
    </section>
    <section class="contacto">
        <Contacto/>
    </section>
</template>

<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background-color: black;
  color: white;
  font-family: Arial, sans-serif;
  height: 100vh; /* Establecemos la altura del body como 100vh */
}

.inicio {
  background-color: black;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 100%; /* Cambiamos la altura a 100% para ocupar toda la pantalla */
  width: 100%;
}

.contenedor-img {
  flex: 1;
}

.contenedor-img img {
  display: flex;
  width: auto;
  height: 90%;
  flex-direction: column;
  align-items: center;
  position: absolute;
  left: 0%;
  top: 10%; 
  filter: opacity(.5)
}

.texto {
    display: flex;
    flex-direction: column;
    position: absolute;
    align-items: flex-start;
    top: 35%;
    right: 5%;    
}

.texto h1 {
  font-family: 'Montserrat', sans-serif;
  color: #C70039;
  font-size: 110px;
  margin-bottom: 10px;
}

.texto h2 {
  font-family: 'Montserrat', sans-serif;
  color: white;
  font-size: 15px;
  margin-bottom: 10px;
}

.redes {
  margin-top: 20px;
}

.redes a {
    color: #fff;
    display: inline-block;
    text-decoration: none;
    border: 1px solid #fff;
    border-radius: 100%;
    width: 42px;
    height: 42px;
    line-height: 42px;
    margin: 40px 5px;
    font-size: 20px;
    transition: .3s;
}




</style>