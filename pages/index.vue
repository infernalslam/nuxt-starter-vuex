<template>
  <div>
    <!-- <h1>{{ $store.state.counter }}</h1> -->
    <counter-display></counter-display>
    <button @click="increment()">+</button>
    <button @click="decrement()">-</button>
  </div>
</template>

<script>
import { mapActions } from 'vuex'
import counterDisplay from '~/components/counterDisplay'
export default {
  data () {
    return {
      counter: 0
    }
  },
  methods: {
    increment () {
      this.counter++
    },
    ...mapActions([
      'increment',
      'decrement'
    ])
  },
  components: {
    counterDisplay
  }
}
</script>
