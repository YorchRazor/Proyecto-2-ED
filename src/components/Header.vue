<template>

 <header>   

  <ul>
            <center>
            <li><a href="index.html">Inicio</a></li>
			 <li><a href="entradas/hacer.html">Apuntes</a></li>
			 <li><a href="entradas/mas.html">Contacto</a></li>
            </center>
        </ul>

</header> 

</template>

<script>
export default {
    data(){
        return{
            title: 'bienvenido'
        }
    }
}
</script>

<style scoped>


header{
    position: absolute;
    width:100%;
    height:50px;
	top: 0;
    left: 0;
    z-index: 0;
    background-color: rgba(8, 95, 177, 0.5);

}

header ul{
    list-style: none;
    top: 0px;
    margin-bottom: 0px
}

header ul li{
    display: inline;
    margin-right: 10px;
    font-style: italic;
    font-weight: bold;
}

header ul li a{
	
    color: white;
    text-decoration: none;
    padding: 10px;
    border-radius: 10px;
    transition: background 300ms;

}

header ul li a:hover {
    background-color: rgb(52, 116, 255);
	
}

header ul li a:active {
    background-color: rgba(160, 157, 5, 0.836);

}



</style>