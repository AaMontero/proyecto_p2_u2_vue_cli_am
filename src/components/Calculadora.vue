<template>
  <h2>Calculadora</h2>
  <label for="pNumero">1er Numero: </label>
  <input type="text" name="pNumero" v-model="numero1" />
  <br />
  <label for="pNumero">2do Numero: </label>
  <input type="text" name="pNumero" v-model="numero2" />
    <div id = "botones">
    <button v-on:click="sumar()">SUMAR</button>
    <button v-on:click="restar()">RESTAR</button>
    <button v-on:click="multiplicar()">MULTIPLICAR</button>
    <button v-on:click="dividir()">DIVIDIR</button>
  </div>
    <label for="idResulado"> Resultado: {{resultado}}</label>
</template>

<script>
export default {
  data() {
    return {
      numero1:"",
      numero2:"",
      resultado:""
    };
  },
  methods: {
    sumar() {
      this.resultado = parseInt(this.numero1) + parseInt(this.numero2);
    },
    restar(){
        this.resultado = parseInt(this.numero1) - parseInt(this.numero2); 
    },
    multiplicar(){
        this.resultado = parseInt(this.numero1) * parseInt(this.numero2); 
    }, 
    dividir(){
        this.resultado = parseInt(this.numero1)/ parseInt(this.numero2); 
    }
  },
};
</script>

<style>

button{
    background-color: skyblue;
    border-radius: 5px;
    color: white; 
    margin: 0 5px;
    cursor: pointer;
}
button:hover{
    background-color: green;
    transition:0.9s ease-in-out;
}
label{
    margin: 2px;
    border-top: 2px;
}
#botones{
    margin:2em
}
</style>