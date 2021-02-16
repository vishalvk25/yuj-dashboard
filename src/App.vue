<template>
  <Navbar msg="Welcome to Your Vue.js App"/>
  <Dashboard msg="Welcome to Your Vue.js App"/>
</template>

<script>
import Dashboard from './components/Dashboard.vue'
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Dashboard,
    Navbar
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
  /* margin-top: 60px; */
}
.common-card {
    font-size: 12px;
}
</style>
