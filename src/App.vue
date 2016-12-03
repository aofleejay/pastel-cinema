<template>
  <div id="app">
    <img src="./assets/logo.png">
    <cinema :seats="seats"></cinema>
    <span>price: {{ totalPrice }}</span>
  </div>
</template>

<script>
  import Cinema from './components/Cinema'

  export default {
    components: {
      Cinema
    },
    computed: {
      totalPrice: function () {
        return this.seats.filter(seat => seat.isBooked).reduce((totalPrice, seat) => totalPrice + seat.price, 0)
      }
    },
    data () {
      return {
        seats: [
          {
            title: 'seat1',
            isBooked: false,
            price: 80
          },
          {
            title: 'seat2',
            isBooked: false,
            price: 80
          },
          {
            title: 'seat3',
            isBooked: false,
            price: 80
          }
        ]
      }
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
