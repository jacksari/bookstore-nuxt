<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <h2>Counter {{ counter }}</h2>
      <v-btn
        depressed
        color="primary"
        @click="increment"
      >
        Increment
      </v-btn>
      <v-btn
        depressed
        color="error"
        @click="decrement"
      >
        Decrement
      </v-btn>
    </v-col>
  </v-row>
</template>

<script>

import { mapMutations } from 'vuex';

export default {
  computed: {
    counter () {
      return this.$store.state.counter
    }
  },
  methods: {
    ...mapMutations({
      increment: 'increment',
      decrement: 'decrement'
    })
  }
}


</script>
