<template>
    <div class="general">
        <div class="sobremi">
            <div class="contenido-seccion" id="sobremi">
                <h2>Sobre Mí</h2>
                <p><span>Hola, soy Manuel Rodas.</span> "Nunca rendirse", es una frase que me defina como persona, podre no ser perfeccto pero siempre estoy dispuesto a mejorar tanto laboral como personal. Soy un estudiante que se encuentra cursando 3 año en la Universidad del valle de Guatemala, en la carrera de ingenieria en ciencias de la computacion</p>

                <div class="fila">
                    <!-- datos personales -->
                    <div class="col">
                        <h3>Datos Personales</h3>
                        <ul>
                            <li>
                                <strong>Nacimiento</strong>
                                13-02-2003
                            </li>
                            <li>
                                <strong>Teléfono</strong>
                                502 51278345
                            </li>
                            <li>
                                <strong>Email</strong>
                                rodasmanuel1@gmial.com
                            </li>
                            <li>
                                <strong><Git-Hub></Git-Hub></strong>
                                https://github.com/ManuelR11
                            </li>
                            <li>
                                <strong>Nacionalidad</strong>
                                Guatemala / Ciudad de Guatemala
                            </li>
                            <li>
                                <strong>Cargo</strong>
                                <span>FULL STACK</span>
                            </li>
                        </ul>
                    </div>
                </div>  
            </div>  
            <button>
                 <i class="fa-solid fa-download"></i>
                <span class="overlay"></span>
            </button>
        </div>  
    </div>
</template>

<style scoped> 

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');
.general{
    background-color: black;
    color: white;
    height: 100vh;
    width: 100%;
    margin-top: -55%;
    justify-content: center;
    align-items: center;
}
.sobremi .contenido-seccion{
    max-width: 1100px;
    height: 100%;
    margin: auto; 
    
}
.sobremi h2{
    color: #C70039;
    font-size: 48px;
    font-family: 'Montserrat', sans-serif;
    text-align: center;
    padding: 20px 0;

}
.sobremi .contenido-seccion p{
    font: 18px;
    line-height: 22px;
    margin-bottom: 20px;
}
.sobremi .contenido-seccion p span{
    color: #C70039;
    font-weight: bold;
}
.sobremi .fila{
    display: flex;
}
.sobremi .fila .col
{
    width: 50%;
}
.sobremi .fila .col h3{
    font-size: 28px;
    font-family: 'Righteous';
    margin-bottom: 25px;
}
.sobremi .fila .col ul{
    list-style: none;
}
.sobremi .fila .col ul li{
    margin: 12px 0;
}
.sobremi .fila .col ul li strong{
    display: inline-block;
    color: #C70039;
    width: 130px;
}
.sobremi .fila .col ul li span{
    background-color: #C70039;
    padding: 3px;
    font-weight: bold;
    border-radius: 5px;
}
.sobremi button {
  cursor: pointer;
  background-color: transparent;
  display: flex;
  flex-direction: column;
  position: absolute;
  align-items: flex-start;
  top: 155%;
  right: 5%;
  width: fit-content;
  display: block;
  margin: 20px auto;
  padding: 10px 22px;
  font-family: 'Montserrat', sans-serif;
  font-size: 75px;
  color: white;
  z-index: 10;
  border: none; /* Eliminamos el borde */
  border-radius: 5px;
}

.sobremi button::before {
  content: "Descargar CV"; /* Texto original del botón */
}
.sobremi button:hover::before {
  color: black;
  content: "Descargar CV"; /* Texto que se mostrará al pasar el mouse */
  font-size: 75px;
}

.sobremi button .overlay{
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    background-color: #C70039;
    z-index: -1;
    transition: 1s;
}
.sobremi button:hover .overlay{
    width: 100%;
}


</style>