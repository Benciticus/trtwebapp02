<template>
<h1>TRT Webapp</h1>
<Phrase/>
</template>

<script>
import Phrase from './components/Phrase.vue'

export default {
  name: 'App',
  components: {
    Phrase
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
