<template>
  <div id="app">
    <main>
      <img alt="Vue logo" src="./assets/logo.png">
      <img alt="Vue logo" src="./assets/logo.png">
      <img alt="Vue logo" src="./assets/logo.png">
      <img alt="Vue logo" src="./assets/logo.png">
      <img alt="Vue logo" src="./assets/logo.png">
      <img alt="Vue logo" src="./assets/logo.png">
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
body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100vw;
  justify-content: space-between;
}

main {
  height: calc(100vh - 76px);
  overflow: auto;
}
</style>
