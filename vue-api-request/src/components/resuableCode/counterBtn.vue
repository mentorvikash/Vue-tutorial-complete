<template>
    <button class="count-button" @click="incrementCount">
        button already {{ count }} times clicked
    </button>
</template>

<script>
import counterFunc from "./../../mixins/counter.js"

export default {
    name: "countBtn",
    mixins: [counterFunc]

    // data() {
    //     return {
    //         count: 0
    //     }
    // },
    // methods: {
    //     incrementCount() {
    //         this.count += 1
    //     }
    // }
}
</script>

<style scoped>
.count-button {
    padding: 10px;
    border: 1px solid black;
    border-radius: 15px;
    font-weight: 600;
    font-size: 20px;
}
</style>