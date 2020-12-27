<template>
  <div id="app">
    <Header />

    <div class="d-flex">
      <img
        src="./assets/logo2.png"
        align="left"
        style="max-width:120px;width:auto;height:auto;"
      />
      <Test class="mx-auto"/>
      <img
        src="./assets/logo.png"
        align="right"
        style="max-width:120px;width:auto;height:auto;"
      />

      
    </div>

    <Footer />
  </div>
</template>

<script>
import Test from "./components/Test.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Test,
    Header,
    Footer
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  margin: 20px;
  padding: 10px;
  background-size: cover;
  background-image: url(./assets/fondo.jpg);
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
}
.d-flex{
  display: flex;
  align-items: center;

}
.mx-auto{
  margin: 0 auto;

}
</style>
