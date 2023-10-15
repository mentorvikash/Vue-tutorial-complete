<template>
    <div>
        <h2>PopUp Element is here</h2>
        <input type="text" v-model="username" />
        <!-- <button @click="$emit('close', 'vikash')">Close Button</button> -->
        <button @click="$emit('close', username)">Close Button</button>

    </div>
</template>

<script>
export default {
    name: 'PopupElement',
    data() {
        return {
            username: '',
        }
    },
    // emits: ['close']
    emits: {
        close(name) {
            if (!name) {
                return false
            } else {
                return true
            }
        }
    }
}
</script>

<style scoped></style>

<!-- We can also add validation with to what action to be emit and what value to be passed -->