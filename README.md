# Proyecto-Final-STW
Proyecto final donde se trabajara un portafolio personal con uso de la tecnologia Vue

## Requerimientos:

Deben crear un portafolio demostrando las tecnologías web que conocen. Pueden utilizar los labs hechos durante el curso o pueden utilizar proyectos personales para respaldar sus conocimientos. Su portafolio es su carta de presentación personal y profesional al solicitar trabajos en el área de web y será evaluado como tal. Voy a tomar en cuenta tanto la estética como las tecnologías que utilicen y la calidad de su código. Supongan que están aplicando a un trabajo en donde la descripción del puesto son los temas vistos en clase. Recuerden que pueden enviar su trabajo cuantas veces quieran siempre que el curso no haya terminado.



## Link de Portafolio:

https://proyecto-3-stw.web.app/

## Link documentación:

https://docs.google.com/document/d/1fH0xGdx7f_CZwFeWq6qCHDYplWPNL1104kR2naJj3Lo/edit?usp=sharing

## Tecnologias utilizadas

- **Vue** — v3.3.4
- **Vite**  — Hot Reloading, Code Splitting, Optimized Build
- **JS** - Components
- **CSS** — Styled Components, CSS

## Getting started

1. Clonar repositorio `https://github.com/ManuelR11/Proyecto-Final-STW`
2. Moverse al directorio: `cd proyecto-2-STW`.<br />
3. Correr `npm install` para instalar dependencias.<br />
4. Correr `npm run dev` para ver la página y correrla en el servidor personal (proporcionado por vite).

## Estructura

- `TableTreck` carpeta donde se encuentra la configuracion (package.json, webpack)
- - `src` carpeta donde se encuentra los archivos .vue .js y .css
- - - `assets` carpeta donde se encuentran las fuentes, imagenes y vectores
- - - `componentes` carpeta donde se encuentran los componentes del proyecto
- - - `App.vue` archivo donde se reciben los componentes del proyecto
- - - `main.js` archivo donde se realiza la navegación de la página
- - `index.html` archivo donde se recibe el script de la página


### Codigo general de componente en Vue

```
<template>
  <!--
    Estructura visual del component
  -->
</template>

<script>
// Importacion de componentes o dependencias
export default {
  data() {
    return {
      // Variables a utilizar en en el template
    }
  },
  components: {
    // Componentes a utilizar en el template
  },
  setup() {
    const router = useRouter();
    const isLogged = false;
    return { router, isLogged };
  },
  methods: {
    // Metodos a utlizar en template
  },
  props:{
    // Propiedades que requiere el componente
  }
  onMounted(){
    // Al montar el DOM
  }
  beforeDestroy(){
    // Lo que sucedera al cerrar el DOM
  }
}

</script>

<style>
    /**
      Aplicar estilos aqui
    */
</style>
```


### Como llamar el componente de vue a un JS

```
import './assets/main.css';

import { createApp } from 'vue';
import { createRouter, createWebHistory } from 'vue-router';

//Importar componentes para el router
import App from './src/App.vue'

// Importa dependencias necesarias


const router = createRouter({
  history: createWebHistory(),
  routes: [
    // Se coloca el path que se desea y el componente al que se debe dirigir el path
    { path: '/', component: App},
  ]
});

// Crea una instancia de Vuetify
const vuetify = createVuetify();

// Creacion de App que utilice nuestro componente principal y nuestro router
createApp(App).use(router).use(vuetify).mount('#app');
```

### Estructura del Index.html
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <link rel="icon" href="/favicon.ico">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="/food-outline.png">
    <title>TableTrek</title>
  </head>
  <body>
    <div id="app"></div>
    <script type="module" src="/src/main.js"></script>
  </body>
</html>
```
