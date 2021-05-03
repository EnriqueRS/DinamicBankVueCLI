<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <tittle text="My dinamic Bank 2.0"></tittle>
</template>

<script>
import Tittle from './components/Tittle'

export default {
  name: 'App',
  components: {
    Tittle
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
