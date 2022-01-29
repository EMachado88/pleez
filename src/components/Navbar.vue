<template>
  <nav>
    <router-link to="/top-up">
      <img src="../assets/topup.png" alt="Top up">
      <p>
        Top up
      </p>
    </router-link>
    <router-link to="/account">
      <img src="../assets/account.png" alt="Account">
      <p>
        Account
      </p>
    </router-link>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: {
    msg: String
  }
}
</script>

<style>
nav {
  display: flex;
  justify-content: space-between;
  height: 76px;
  background-color: #fff;
}

nav > a {
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-decoration: none;
}

p {
  margin: 0;
  font-size: 12px;
}
</style>
