<template>
  <!--<img alt="Vue logo" src="./assets/logo.png" />-->
  <Pregunta />
  <h1></h1>
  <h1></h1>
</template>

<script>
import Contador from "./components/Contador.vue";
import Contador2 from "./components/Contador2.vue";
import DatosBasios from "./components/DatosBasicos.vue";
import Calculadora from "./components/Calculadora.vue";
import Pregunta from "./components/Pregunta.vue";
export default {
  name: "App",
  data() {
    return {
      valorInicio: 27,
      tipo: "Estudiante",
    };
  },
  components: {
    Contador,
    Contador2,
    Calculadora,
    DatosBasios,
    Pregunta,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
