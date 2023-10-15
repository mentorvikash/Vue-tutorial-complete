<template>
    <div>
        <input type="text" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)">
    </div>
</template>

<script>
export default {
    name: "InputElement",
    props: {
        modelValue: String
    }
}
</script>

<style scoped></style>