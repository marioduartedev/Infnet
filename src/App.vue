<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <HelloWorld msg="Hello!"/>
    <div class="horas">
      <p v-if="horas < 12">Está de dia!</p>
      <p v-if="horas >= 12 && horas < 18">Está de tarde!</p>
      <p v-if="horas >= 18">Está de noite!</p>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }, data(){
    return { 
      title : "Locadora de Filmes",
      horas : new Date().getHours(),
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
