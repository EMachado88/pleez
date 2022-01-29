<template>
  <div class="account">
    <div class="header container">
      <p class="white">Hello {{ name }}!</p>
    </div>

    <div class="sub-header container">
      <p>Your Banana credits!</p>
    </div>

    <div class="container">
      <a class="btn btn-reverse full-width">
        {{ balance }}€
      </a>
    </div>

    <div class="container">
      <h4>Past Top Ups</h4>

      <table>
        <tr>
          <td>Date</td>
          <td>Value</td>
        </tr>
      </table>

      <p class="text-center">No past top ups</p>
    </div>
  </div>
</template>

<script>
import data from '../data.json'

export default {
  name: 'Account',
  data() {
    return {
      name: data.account.name,
      balance: data.account.balance,
      selectedPaymentMethod: '',
      paymentMethods: data.paymentMethods,
    }
  },
  methods: {
    selectPaymentMethod(type) {
      this.selectedPaymentMethod = type
    },
    topUp() {
      this.amount = ''
      this.selectedPaymentMethod = ''
    }
  }
}
</script>

<style scoped>
.header {
  margin-top: 115px;
}

table {
  width: 100%;
}
</style>
