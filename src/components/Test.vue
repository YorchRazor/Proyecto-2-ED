<template>


  <div>
      <h1>Proyecto de Estructura Discretas</h1>
      <h2>Intruduzca la expresión que desea evaluar</h2>
    <input type="text" v-model="cadena" />
    <button type="button" v-on:click="show = true">
      CLIQUEAME
    </button>

<!--FALLOS AL IMPRIMIR (pvq) DEBERIA IMPRIMIR SOLO false en el ultimo-->

    <div v-if="show">
      <Tabla :p="true" :q="true" :cadena="cadena" />
      <Tabla :p="true" :q="false" :cadena="cadena" />
      <Tabla :p="false" :q="true" :cadena="cadena" />
      <Tabla :p="false" :q="false" :cadena="cadena" />
    </div>
  </div>
</template>

<script>
import Tabla from "./Tabla"
export default {
    components:{
        Tabla
    },
  data() {
    return {
      show: false,
      cadena: "",
    };
  }
};
</script>

<style>

h1{
    padding: 10px;
    text-align: center;
    font-size: 35px;
    font-family: arial;
    color: rgb(22, 115, 146);
    text-shadow: 0px 0px 3px white;
}

h2{
    padding: 10px;
    text-align: center;
    font-size: 25px;
    font-family: arial;
    color: rgb(204, 185, 12);
    text-shadow: 0px 0px 3px white;
}
</style>
