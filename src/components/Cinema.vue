<template>
  <div>
    <h1>{{ title }}</h1>
    <seat v-for="seat in seats" :seat="seat"></seat>
  </div>
</template>

<script>
  import Seat from './Seat'

  export default {
    name: 'cinema',
    props: ['seats'],
    components: {
      Seat
    },
    data () {
      return {
        title: 'Pastel Cinema'
      }
    }
  }
</script>

<style scoped>
  h1 {
    text-align: center;
  }
</style>