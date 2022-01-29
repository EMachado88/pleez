<template>
  <div class="home">
    <div class="header">
      <img src="../assets/banana-cafe.png" alt="Banana Cafe">
    </div>

    <router-link to="/account" class="btn full-width">Account</router-link>
    <router-link to="/top-up" class="btn full-width">Top Up</router-link>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped>
.header {
  text-align: center;
  margin-top: 80px;
  margin-bottom: 160px;
}
</style>
