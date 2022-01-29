<template>
  <div id="app">
    <main>
      <div class="header">
        <img src="./assets/banana-cafe.png" alt="Banana Cafe">
      </div>

      <button class="w-100">Account</button>
      <button class="w-100">Top Up</button>
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
}

button {
  background-color: #000;
  border-color: #000;
  color: #fff;
  border-radius: 10px;
  font-size: 24px;
  padding: 20px;
  text-transform: uppercase;
  margin-bottom: 15px;
}

button:hover {
  background-color: #fff;
  border-color: #000;
  color: #000;
}

main {
  height: calc(100vh - 76px);
  overflow: auto;
  max-width: 340px;
  width: 100%;
  margin: auto;
}

.header {
  text-align: center;
  margin-top: 80px;
  margin-bottom: 160px;
}
</style>
