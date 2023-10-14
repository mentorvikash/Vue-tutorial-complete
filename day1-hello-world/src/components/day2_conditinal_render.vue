<template>
    <h2 v-if="count === 0"> if block: Number is Zero</h2>
    <h2 v-else-if="count > 0">else if block: Number is grater then zero</h2>
    <h2 v-else-if="count < 0">else if block: Number is Less then zero</h2>
    <h2 v-else>else block if non condition meet: Not a Number</h2>
    <template v-if="ifvisible">
        <h3>we have to display</h3>
        <h3>A number of items</h3>
        <h3>based on some condition</h3>
    </template>
    <h2 v-show="isvisible">v-show used to show element and remain in dom ui if not visible</h2>
    <h2 v-if="isvisible">v-if used to show element and get removed from dom tree if condition not match</h2>
</template>
  
<script>
export default {
    name: "App",
    data() {
        return {
            count: "fdfa",
            ifvisible: true,
            isvisible: true,
        };
    },
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

.underline {
    text-decoration: underline;
}

.success {
    color: green
}

.promoted {
    font-style: italic;
}

.new {
    color: orchid
}

.sold-out {
    color: red;
}

.box-wraper {}
</style>
  