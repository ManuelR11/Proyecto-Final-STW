<template>
    <div class="contenedor-header">
        <header>
            <div class="logo">
                <a href="#">Rodas</a>
            </div>
            <nav id="nav">
                <ul>
                    <li><a href="#inicio" onclick="seleccionar()">INICIO</a></li>
                    <li><a href="#sobremi" onclick="seleccionar()">SOBRE MI</a></li>
                    <li><a href="#skills" onclick="seleccionar()">SKILLS</a></li>
                    <li><a href="#curriculum" onclick="seleccionar()">Extra-Curriculum</a></li>
                    <li><a href="#portfolio" onclick="seleccionar()">PORTFOLIO</a></li>
                    <li><a href="#contacto" onclick="seleccionar()">CONTACTO</a></li>
                </ul>
            </nav>
            <div class="nav-responsive" onclick="mostrarOcultarMenu()">
                <i class="fa-solid fa-bars"></i>
            </div>
        </header>
    </div>
</template>


<style>

@import url('https://fonts.googleapis.com/css2?family=Righteous&family=Work+Sans:wght@100;300;400;600;800&display=swap');
*{
    box-sizing: border-box;
    font-family: 'Work Sans';
    margin: 0;
    padding: 0;
}
.contenedor-header{
    background: black;
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    z-index: 99;
}
.contenedor-header header{
    max-width: 1100px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 20px;
}
.contenedor-header header .logo a{
    font-family: 'Righteous';
    font-size: 36px;
    color: black;
    text-decoration: none;
}
.contenedor-header header ul{
    display: flex;
    list-style: none;
}
.contenedor-header header nav ul li a{
    text-align: none;
    color: #fff;
    margin: 0 15px;
    padding: 3px;
    transition: .5s;
    text-decoration: none;
}
.contenedor-header header nav ul li a:hover{
    color: #C70039;
}
.nav-responsive{
    background-color: #C70039;
    color:#fff;
    padding: 5px 10px;
    border-radius: 5px;
    cursor: pointer;
    display: none;
}



</style>