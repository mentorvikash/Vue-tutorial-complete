<template>
  <h1>Methods in Vuejs</h1>
  <h2>sum of number : {{ 5 + 42 + 25 }}</h2>
  <h2>adding of two string: {{ "firstname" + " " + "lastname" }}</h2>
  <h2>Addtion by add method: {{ add(10, 5) }}</h2>
  <h2>subtraction by sub method: {{ sub(10, 5) }}</h2>
  <h2>multitiply by multiple method: {{ multiple(12) }}</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      baseNumber: 12
    }
  },
  methods: {
    add(a, b) {
      return a + b;
    },

    sub(a, b) {
      return a - b;
    },

    multiple(num) {
      return this.baseNumber * num;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
