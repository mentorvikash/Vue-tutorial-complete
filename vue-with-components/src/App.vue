<template>
  <LetGreet name="Amar" fruit="Mango" />
  <LetGreet name="Rajat" fruit="Papaya" />
  <LetGreet name="Vishal" fruit="Orange" />
  <LetGreet :name="name" :fruit="fruit" />
</template>

<script>
import LetGreet from './components/greet.vue'

export default {
  name: 'App',
  data() {
    return {
      name: 'Revive',
      fruit: 'Coding'
    }
  },
  components: {
    LetGreet
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
