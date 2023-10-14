<template>
  <h1>Event Lisners with Counter App</h1>
  <h2>{{ count }}</h2>
  <!-- <div class="button-parent">
    <button v-on:click="count += 1">Increment</button>
    <button v-on:click="count -= 1">Decrement</button>
  </div> -->
  <div class="button-parent">
    <button v-on:click="decrement">Decrement</button>
    <button v-on:click="increment">Increment</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count = this.count + 1;
    },
    decrement() {
      if (this.count != 0) {
        this.count -= 1
      }
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

.button-parent {
  display: flex;
  padding: 10px;
  background-color: gainsboro;
  justify-content: center;
  gap: 12px;
}

.button-parent button {
  padding: 5px;
  color: white;
  background: blue;
  border: "1px solid black";
  border-radius: 5px;

  &:hover {
    color: black;
    background: white
  }
}
</style>
