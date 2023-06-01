<template>
 <div class="container_general">   
    <div class="contenido-seccion" id="skills">
            <h2>Skills</h2>
            <div class="fila">
                <div class="col">
                    <h3>Technical Skills</h3>
                    <div class="skill">
                        <span>Javascript</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>75%</span>
                            </div>
                        </div>
                    </div>
                    <div class="skill">
                        <span>HTML & CSS</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>89%</span>
                            </div>
                        </div>
                    </div>
                    <div class="skill">
                        <span>Photoshop</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>95%</span>
                            </div>
                        </div>
                    </div>
                    <div class="skill">
                        <span>Wordpress</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>81%</span>
                            </div>
                        </div>
                    </div>
                    <div class="skill">
                        <span>Drupa</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>55%</span>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Professional Skills -->
                <div class="col">
                    <h3>Professional Skills</h3>
                    <div class="skill">
                        <span>Comunicación</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>80%</span>
                            </div>
                        </div>
                    </div>
                    <div class="skill">
                        <span>Trabajo en Equipo</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>70%</span>
                            </div>
                        </div>
                    </div>
                    <div class="skill">
                        <span>Creatividad</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>99%</span>
                            </div>
                        </div>
                    </div>
                    <div class="skill">
                        <span>Dedicación</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>65%</span>
                            </div>
                        </div>
                    </div>
                    <div class="skill">
                        <span>Proyect Management</span>
                        <div class="barra-skill">
                            <div class="progreso">
                                <span>94%</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { onMounted } from 'vue';

onMounted(() => {
  efectoHabilidades();
});

function efectoHabilidades() {
  const skills = document.getElementById('skills');
  const distanciaSkills = window.innerHeight - skills.getBoundingClientRect().top;
  if (distanciaSkills >= 300) {
    const habilidades = document.getElementsByClassName('progreso');
    habilidades[0].classList.add('javascript');
    habilidades[1].classList.add("htmlcss");
    habilidades[2].classList.add("photoshop");
    habilidades[3].classList.add("wordpress");
    habilidades[4].classList.add("drupal");
    habilidades[5].classList.add("comunicacion");
    habilidades[6].classList.add("trabajo");
    habilidades[7].classList.add("creatividad");
    habilidades[8].classList.add("dedicacion");
    habilidades[9].classList.add("proyect");
  }
}
</script>


<style scoped>  
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');
.container_general{
    margin-top: -5%;
    height: 100vh;
    width: 200%;
    justify-content: center;
    align-items: center;
}

.skills h2{
    font-size: 78px;
    color: #C70039;
    font-family: 'Montserrat', sans-serif;
    text-align: center;
    padding: 20px 0;

}
.skills .fila{
    display: flex;
}
.skills .fila .col{
    width: 50%;
    padding: 0 20px;
}
.skills .fila .col h3{
    font-size: 28px;
    font-family: 'Righteous';
    margin-bottom: 25px;
}
.skills .skill > span{
    font-weight: bold;
    display: block;
    margin-bottom: 10px;
}
.skills .skill .barra-skill{
    height: 8px;
    width: 80%;
    background-color: #131517;
    position: relative;
    margin-bottom: 30px;
}
.skills .skill .progreso{
    background-color: #C70039;
    position: absolute;
    top: 0;
    left: 0;
    height: 8px;
}
.skills .skill .barra-skill span{
    position: absolute;
    height: 40px;
    width: 40px;
    background-color: #C70039;
    border-radius: 50px;
    line-height: 40px;
    text-align: center;
    top: -17px;
    right: -15px;
    font-size: 14px;
}
/* Estas clases se agregaran dinamicamente mediante javascript */
.skills .skill .javascript{
    width: 0%;
    animation: 2s javascript forwards;
}
@keyframes javascript {
    0%{width: 0%;}
    100%{width: 75%;}
}

.skills .skill .htmlcss{
    width: 0%;
    animation: 2s htmlcss forwards;
}
@keyframes htmlcss {
    0%{width: 0%;}
    100%{width: 89%;}
}

.skills .skill .photoshop{
    width: 0%;
    animation: 2s photoshop forwards;
}
@keyframes photoshop {
    0%{width: 0%;}
    100%{width: 95%;}
}

.skills .skill .wordpress{
    width: 0%;
    animation: 2s wordpress forwards;
}
@keyframes wordpress {
    0%{width: 0%;}
    100%{width: 81%;}
}

.skills .skill .drupal{
    width: 0%;
    animation: 2s drupal forwards;
}
@keyframes drupal {
    0%{width: 0%;}
    100%{width: 55%;}
}

.skills .skill .comunicacion{
    width: 0%;
    animation: 2s comunicacion forwards;
}
@keyframes comunicacion {
    0%{width: 0%;}
    100%{width: 80%;}
}

.skills .skill .trabajo{
    width: 0%;
    animation: 2s trabajo forwards;
}
@keyframes trabajo {
    0%{width: 0%;}
    100%{width: 70%;}
}

.skills .skill .creatividad{
    width: 0%;
    animation: 2s creatividad forwards;
}
@keyframes creatividad {
    0%{width: 0%;}
    100%{width: 99%;}
}

.skills .skill .dedicacion{
    width: 0%;
    animation: 2s dedicacion forwards;
}
@keyframes dedicacion {
    0%{width: 0%;}
    100%{width: 65%;}
}

.skills .skill .proyect{
    width: 0%;
    animation: 2s proyect forwards;
}
@keyframes proyect {
    0%{width: 0%;}
    100%{width: 94%;}
}
</style>