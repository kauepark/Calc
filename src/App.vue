<template>
  <div id="app">
    <input id="val1" type="text" placeholder="Digite um valor">
    <hr>
    <input id="val2" type="text" placeholder="Digite outro valor">
    <hr>
    <button v-on:click="somar">Somar</button>
    <div>
      <h1 id="res">{{resultado}}</h1>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      resultado: ''
    };
  },
  methods: {
    somar: function() {
      this.resultado = parseInt(document.getElementById("val1").value) + parseInt(document.getElementById("val2").value)
      document.querySelector("res").innerHTML = this.resultado
    }
  }
}
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