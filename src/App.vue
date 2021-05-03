<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <tittle text="My dinamic Bank 2.0"></tittle>
  <bank-account></bank-account>
</template>

<script>
import Tittle from './components/Tittle'
import BankAccount from './components/BankAccount'

export default {
  name: 'App',
  components: {
    Tittle,
    BankAccount
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
