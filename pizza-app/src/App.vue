<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <PizzaPage msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import PizzaPage from './components/PizzaPage.vue'

export default {
  name: 'App',
  components: {
    PizzaPage
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
