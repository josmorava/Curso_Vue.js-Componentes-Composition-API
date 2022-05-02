<template>
  <div class="">
    <home-component first-name='Jose' last-name='Varon'/>
  </div>

</template>

<script>
import HomeComponent from './components/HomeComponent.vue'

import {provide} from 'vue' 

export default {
  name: 'App',
  //mixins:[base],
  components: {
    HomeComponent
  },

  setup() {
    provide('username', 'JosMoraVa')
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
