<template>
  <div id="app">
    <main>
      <router-view />
    </main>
    <Navbar msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style>
@import './assets/fonts/stylesheet.css';
@import './assets/styles/reset.css';
@import './assets/styles/helpers.css';

body {
  margin: 0;
}

#app {
  font-family: Poppins, Helvetica, Arial, sans-serif !important;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100vw;
  justify-content: space-between;
  background-color: #F4C935;
  font-size: 24px;
}

.btn {
  background-color: #000;
  border-color: #000;
  color: #fff;
  border-radius: 10px;
  font-size: 24px;
  padding: 20px;
  text-transform: uppercase;
  text-align: center;
  text-decoration: none;
  margin-bottom: 15px;
}

.btn:hover {
  background-color: #fff;
  border-color: #000;
  color: #000;
}

.btn.full-width {
  display: block;
}

main {
  height: calc(100vh - 76px);
  overflow: auto;
  max-width: 340px;
  width: 100%;
  margin: auto;
}
</style>
