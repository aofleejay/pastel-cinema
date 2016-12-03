<template>
  <div class="seat" :class="{ booked: seat.isBooked }" @click="toggleSeat()">
    <h2>{{ seat.title }}</h2>
  </div>
</template>

<script>
export default {
  props: ['seat'],
  methods: {
    toggleSeat () {
      this.seat.isBooked = !this.seat.isBooked
    }
  }
}
</script>

<style scoped>
  .seat {
    text-align: center;
    padding: 10px 15px;
    margin: 0 5px;
    display: inline-block;
    background-color: #00FF00;
  }
  .booked {
    background-color: #FF0000;
    color: #FFFFFF;
  }
</style>