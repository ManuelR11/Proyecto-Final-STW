<template>
    <div class="portafolio" id="portfolio">
      <h2>Portafolio</h2>
      <table class="cartas">
        <tr>
          <td>
            <Card
              image="https://image-pastemagazine-com-public-bucket.storage.googleapis.com/wp-content/uploads/2022/08/17124429/snake_coolmath.jpg"
              title="Arcade Game"
              description="Este proyecto incluye dos juegos clásicos de arcade: Tetris y Snake. Ambos juegos fueron desarrollados utilizando Angular, Node.js y firebase."
              :buttons="[
                { label: '+', url: 'https://proyecto-2-stw.web.app/app' },
                { label: 'GIT', url: 'https://github.com/ManuelR11/Proyecto2_SistemasWeb' }
              ]"
            />
          </td>
          <td>
            <Card
              image="https://static.vecteezy.com/system/resources/previews/012/039/733/non_2x/css-letter-logo-design-with-black-background-in-illustrator-logo-modern-alphabet-font-overlap-style-calligraphy-designs-for-logo-poster-invitation-etc-vector.jpg"
              title="Dibujo en CSS"
              description="Se replico una imagen con la utilizacion exclusiva de css"
              :buttons="[
                { label: '+', url: 'http://54.145.70.177:3162/' },
                { label: 'GIT', url: 'https://github.com/ManuelR11' }
              ]"
            />
          </td>
        </tr>
        <tr>
          <td>
            <Card
              image="https://thumbs.dreamstime.com/b/icono-de-base-datos-en-nube-aislado-fondo-negro-logotipo-vectorial-simple-161701042.jpg"
              title="Base de Datos y Pagina Web"
              description="El proyecto contempla el uso de tecnología de Base de Datos para la modelación y creación de una base de datos para un sistema de aplicación"
              :buttons="[
                { label: '+', url: 'https://github.com/Jskenpo/MediCom' },
                { label: 'GIT', url: 'https://github.com/Jskenpo/MediCom' }
              ]"
            />
          </td>
          <td>
            <Card
              image="https://jojoy-app-files.ezjojoy.com/avatar/386381954011578368"
              title="Replica Spotify"
              description="En este proyecto se busco replicar de forma exacta la vista de la pagian web de Spotify"
              :buttons="[
                { label: '+', url: 'https://proyecto-1-stw.web.app' },
                { label: 'GIT', url: 'https://github.com/ManuelR11/Proyecto_1_SistemasWeb/tree/main' }
              ]"
            />
          </td>
        </tr>
      </table>
    </div>
  </template>
  
  <script>
  import Card from './card.vue';
  
  export default {
    components: {
      Card
    }
  };
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');

.portafolio h2 {
  font-size: 78px;
  font-family: 'Montserrat', sans-serif;
  color: #C70039;
}

.cartas {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-left: 15%;
  gap: 30px;
}

.cartas td {
  flex-basis: 50%;
  padding: 10px;
  box-sizing: border-box;
}

@media (max-width: 768px) {
  .cartas td {
    flex-basis: 100%;
  }
}
</style>
