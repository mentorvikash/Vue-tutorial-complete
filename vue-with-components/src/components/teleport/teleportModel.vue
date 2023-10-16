<template>
    <div class="model-main">
        <h3>Sentence 12</h3>
        <h3>Sentence 3</h3>
        <h3>Sentence 14</h3>
        <h3>Sentence 78</h3>
        <h3>Sentence 145451</h3>
    </div>
    <button @click="$emit('close')">Close</button>
</template>

<script>
export default {
    name: "TeleModel",
    emits: ['close']
}
</script>

<style scoped>
.model-main {
    border: 1px sold black;
    box-shadow: 3px 4px 15px black;
    background-color: aquamarine;
    padding: 10px;
}
</style>