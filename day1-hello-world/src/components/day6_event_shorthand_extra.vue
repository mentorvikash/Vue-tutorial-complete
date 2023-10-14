<template>
    <h1>Topic: Short Hand syntex for events </h1>
    <h2>we can replace v-on: with just @</h2>
    <h2>{{ count }}</h2>
    <div class="button-parent">
        <button @click="decrement">Decrement</button>
        <button @click="increment">Increment</button>
    </div>
    <h2>On button click change name and increase counter </h2>
    <h3>{{ name }}</h3>
    <button v-on:click="changeName('Rajat singh', $event), increment($event)">change name</button>
</template>
  
<script>
export default {
    name: "App",
    data() {
        return {
            count: 0,
            name: "vikash singh"
        }
    },
    methods: {
        increment(event) {
            console.log(event)
            this.count = this.count + 1;
        },
        decrement() {
            if (this.count != 0) {
                this.count -= 1
            }
        },
        changeName(name, event) {
            this.name = name
            console.log("evnet:", event)
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
  