<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{word}}</h1>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <HelloWorld :msg="fuck2"/> 
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
let fuck = "diu2";
fetch('https://jsonplaceholder.typicode.com/todos/1')
  .then(response => response.json())
  .then(json => console.log(json))
export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      fuck2 : "diu",
      word : fuck,
    };
  },
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
