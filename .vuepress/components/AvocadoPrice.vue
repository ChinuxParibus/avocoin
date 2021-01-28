<template>
  <div>
    <h1>Avocoin</h1>
    <h2>1 BTC -> {{ price }} 🥑</h2>
  </div>
</template>

<script>
export default {
  name: 'AvocadoPrice',
  data() {
    return {
      price: 0
    }
  },
  created() {
    fetch('https://avocoinapp.herokuapp.com')
    .then(response => response.json())
    .then(data => {
      this.price = data.price
    })
  }
}
</script>
