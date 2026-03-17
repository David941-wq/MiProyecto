<template>
  <div class="espacio">
    <NavegadorVue></NavegadorVue>
  </div>
  <router-view></router-view>
</template>

<script>
import NavegadorVue from './components/NavegadorVue.vue';

export default {
  name: 'App',
  components: {
    NavegadorVue
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
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
.espacio {
  height: 80px;
}
</style>
