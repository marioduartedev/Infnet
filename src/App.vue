<template>
<b-container>
  <b-row>
    <h1>{{ title }}</h1>
  </b-row>
  <b-row>
    <HelloWorld msg="Hello!"/>
  </b-row>
  <b-row>
      <p v-if="horas < 12">Está de dia!</p>
      <p v-if="horas >= 12 && horas < 18">Está de tarde!</p>
      <p v-if="horas >= 18">Está de noite!</p>
  </b-row>
</b-container>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
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
  .row {
    justify-content: center;
  }
</style>
