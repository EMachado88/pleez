<template>
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
</template>

<script>
export default {
  name: 'TopUpsTable',
  props: {
    topUps: Array
  }
}
</script>
