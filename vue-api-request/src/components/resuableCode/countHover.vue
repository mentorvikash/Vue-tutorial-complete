<template>
    <h2 class="count-hover" @mousemove="incrementCount">
        Element Hovered {{ count }} times
    </h2>
</template>

<script>
import counterFunc from "./../../mixins/counter.js"

export default {
    name: "countHover",
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
.count-hover {
    padding: 10px;
    border-radius: 15px;
    font-weight: 600;
    font-size: 20px;
}
</style>