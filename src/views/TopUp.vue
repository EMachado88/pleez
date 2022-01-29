<template>
  <div class="top-up">
    <div class="header container">
      <p class="white">Hello {{ account.name }}!</p>
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
        :class="{ 'selected': selectedPaymentMethod ===  paymentMethod.type}"
        @click="selectPaymentMethod(paymentMethod.type)"
      >
        <img :src="paymentMethod.image" :alt="paymentMethod.label">
        {{ paymentMethod.label }}
      </a>

      <a
        v-if="amount && selectedPaymentMethod"
        class="btn full-width"
        @click="topUp()"
      >
        Pay {{ amount }}€
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TopUp',
  props: {
    account: Object,
    paymentMethods: Array,
    topUps: Array
  },
  data() {
    return {
      amount: '',
      selectedPaymentMethod: ''
    }
  },
  methods: {
    selectPaymentMethod(type) {
      this.selectedPaymentMethod = type
    },
    topUp() {
      this.account.balance += parseFloat(this.amount)
      this.topUps.push({
        date: new Date(),
        value: this.amount,
        type: this.selectedPaymentMethod
      })

      alert(`Successful Top Up!
Method: ${this.selectedPaymentMethod}
Amount: ${this.amount}€`)

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

.sub-header {
  margin: 100px auto;
  text-align: center;
}

.payment-method {
  font-size: 18px;
  background-color: rgba(242, 242, 242, 0.71);
  padding: 15px;
  margin-top: 30px;
  padding-bottom: 30px;
}

.btn-payment {
  border-color: #000;
  text-transform: initial;
  font-size: 16px;
  display: flex;
  align-items: center;
  border-radius: 20px;
}

.btn-payment.selected {
  border-color: #000;
  background-color: #F4C935;
  color: #fff;
}

.btn-payment img {
  width: 38px;
  margin-right: 15px;
}
</style>
