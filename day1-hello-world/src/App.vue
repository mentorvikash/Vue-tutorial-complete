<template>
  <h1>Topic: </h1>
</template>

<script>
export default {
  name: "App",
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
