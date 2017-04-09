<template>
  <div>
    <h1>{{ counter }}</h1>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters([
      'counter'
    ])
  }
}
</script>
