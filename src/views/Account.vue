<template>
  <div class="account">
    <div class="header container">
      <p class="white">Hello {{ account.name }}!</p>
    </div>

    <div class="sub-header container">
      <p>Your Banana credits!</p>
    </div>

    <div class="container">
      <a class="btn btn-reverse full-width">
        {{ account.balance }}€
      </a>
    </div>

    <div class="top-ups container">
      <h4>Past Top Ups</h4>

      <table>
        <tr>
          <td>Date</td>
          <td>Value</td>
        </tr>

        <tr v-for="(topUp, index) in topUps" :key="index">
          <td>{{ topUp.date.toLocaleDateString() }}</td>
          <td>{{ topUp.value }}€</td>
        </tr>
      </table>

      <p v-if="!topUps.length" class="text-center">No past top ups</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Account',
  props: {
    account: Object,
    topUps: Array
  }
}
</script>

<style scoped>
.header {
  margin-top: 115px;
}

.sub-header {
  margin: 100px auto;
  text-align: center;
}

.top-ups {
  margin-top: 100px;
}

table {
  width: 100%;
}
</style>
