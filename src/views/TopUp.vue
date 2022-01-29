<template>
  <div class="top-up">
    <div class="header container">
      <p class="white">Hello {{ name }}!</p>
    </div>

    <div class="sub-header container">
      <p>Top up your Wallet!</p>
    </div>

    <div class="container">
      <input v-model="amount" class="w-100" type="number" placeholder="Amount" />
    </div>

    <div class="payment-method">
      <p class="text-center">Payment Method</p>

      <a
        v-for="(paymentMethod, index) in paymentMethods"
        :key="index"
        class="btn btn-reverse btn-payment full-width"
      >
        <img :src="paymentMethod.image" :alt="paymentMethod.label">
        {{ paymentMethod.label }}
      </a>

      <a class="btn full-width">
        Pay
      </a>
    </div>
  </div>
</template>

<script>
import data from '../data.json'

console.log(data)

export default {
  name: 'TopUp',
  data() {
    return {
      name: data.account.name,
      amount: '',
      paymentMethods: data.paymentMethods
    }
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

.payment-method {
  font-size: 18px;
  background-color: rgba(242, 242, 242, 0.71);
  padding: 15px;
  margin-top: 30px;
}

.payment-method .btn-payment {
  border-color: #000;
  text-transform: initial;
  font-size: 16px;
  display: flex;
  align-items: center;
  border-radius: 20px;
}

.payment-method .btn-payment img {
  width: 38px;
  margin-right: 15px;
}
</style>
