<template>
<the-navbar />
  <div class="container with-nav">
    <div class="card">
      <h1>Про Vuex</h1>
      <h2>Счетчик {{ counter }}</h2>
      <button class="btn" @click="increment">Increment</button>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex' 
import TheNavbar from './TheNavbar.vue'

export default {
  components: { TheNavbar },

  computed: {
    ...mapGetters(['counter'])
  },

  methods: {
    increment() {
      this.$store.commit('increment')
    }
  }
}
</script>
