<template>
    <div class="Hire">
      <button class="Boton_form" @click="toggleFormulario"></button>
      <div v-if="mostrar">
        <form class="formulario" @submit.prevent="enviarFormulario">
          <label for="nombreEmpresa">Nombre de la empresa:</label>
          <input type="text" id="nombreEmpresa" v-model="nombreEmpresa" required>
          <br>
          <label for="motivo">Motivo:</label>
          <textarea id="motivo" v-model="motivo" required></textarea>
          <br>
          <button type="submit">Enviar</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        mostrar: false,
        nombreEmpresa: '',
        motivo: ''
      };
    },
    methods: {
      toggleFormulario() {
        this.mostrar = !this.mostrar;
      },
      enviarFormulario() {
        // Aquí puedes realizar alguna acción con los datos ingresados, como enviarlos a través de una API, etc.
        console.log('Nombre de la empresa:', this.nombreEmpresa);
        console.log('Motivo:', this.motivo);
  
        // Luego, puedes reiniciar el formulario si deseas
        this.nombreEmpresa = '';
        this.motivo = '';
      }
    }
  };
  </script>
  
  <style scoped>
  .Hire {
    margin-left: 15%;
    margin-top: 15%;
    border-radius: 25px;
  }
  
  .Boton_form {
    cursor: pointer;
    background-color: transparent;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: fit-content;
    display: block;
    margin: 20px auto;
    padding: 10px 22px;
    font-family: 'Montserrat', sans-serif;
    font-size: 35px;
    color: white;
    z-index: 10;
    border: none; /* Eliminamos el borde */
    border-radius: 5px;
  }
  
  .Boton_form::before {
    content: "Hire me"; /* Texto original del botón */
  }
  
  .Boton_form:hover::before {
    color: #C70039;
    content: "Hire me"; /* Texto que se mostrará al pasar el mouse */
  }
  
  .Boton_form .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    background-color: #C70039;
    z-index: -1;
    transition: 1s;
  }
  
  .Boton_form:hover .overlay {
    width: 100%;
  }
  
  .formulario {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-top: 20px;
  }
  
  .formulario label {
    font-family: 'Montserrat', sans-serif;
    font-size: 18px;
    color: white;
  }
  
  .formulario input,
  .formulario textarea {
    width: 300px;
    padding: 8px;
    margin-bottom: 10px;
    border-radius: 5px;
    border: 1px solid #ccc;
  }
  .formulario button {
    padding: 10px 20px;
    background-color: #C70039;
    color: white;
    font-family: 'Montserrat', sans-serif;
    font-size: 16px;
    border: none;
    border-radius: 5px;
   
}
</style>