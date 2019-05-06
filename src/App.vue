<template>
  <div>
    <p>click: {{count}} times, count is {{evenOrOdd}}</p>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="incrementIfOdd">increment if odd</button>
    <button @click="incrementAsync">increment async</button>
  </div>
</template>

<script>
import {mapState,mapActions,mapGetters} from 'vuex'
export default {
  name: 'App',
  computed: {
    // evenOrOdd () {
    //   return this.$store.getters.evenOrOdd;
    // }
    ...mapState(['count']),
    ...mapGetters(['evenOrOdd'])
  },
  methods : {
    // increment () {
    //   this.$store.dispatch('increment')
    // },
    // decrement () {
    //   this.$store.dispatch('decrement')
    // },
    // incrementIfOdd () {
    //   this.$store.dispatch('incrementIfOdd')
    // },
    // incrementAsync () {
    //   this.$store.dispatch('incrementAsync')
    // }
    ...mapActions(['increment','decrement','incrementIfOdd','incrementAsync'])
  }
}
</script>

<style>

</style>
