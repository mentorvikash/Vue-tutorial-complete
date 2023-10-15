<template>
    <div>
        <h2>PopUp Element is here</h2>
        <button @click="$emit('close', 'vikash')">Close Button</button>
    </div>
</template>

<script>
export default {
    name: 'PopupElement',
    emits: ['close']
}
</script>

<style scoped></style>