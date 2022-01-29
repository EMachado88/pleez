<template>
  <navbar>
    <div>
      <img src="../assets/topup.png" alt="Top up">
      <h6>
        Top up
      </h6>
    </div>
    <div>
      <img src="../assets/account.png" alt="Account">
      <h6>
        Account
      </h6>
    </div>
  </navbar>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style>
navbar {
  display: flex;
  justify-content: space-between;
  height: 76px;
}

navbar > div {
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h6 {
  margin: 0;
}
</style>
