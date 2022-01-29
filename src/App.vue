<template>
  <div id="app">
    <main>
      <p>Content</p>
    </main>
    <Navbar msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import './assets/fonts/stylesheet.css'

import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: Poppins, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100vw;
  justify-content: space-between;
  background-color: #F4C935;
}

main {
  height: calc(100vh - 76px);
  overflow: auto;
  max-width: 360px;
  width: 100%;
  margin: auto;
}
</style>
