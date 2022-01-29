<template>
  <navbar>
    <div>
      Top up
    </div>
    <div>
      Account
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
  justify-content: center;
  align-items: center;
}
</style>
