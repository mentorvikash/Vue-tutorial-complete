<template>
    <div>
        <InputElement v-model="textValue" />
    </div>
</template>

<script>
import InputElement from './input.vue';
export default {
    name: 'InputMain',
    data() {
        return {
            textValue: ''
        }
    },
    components: {
        InputElement
    },
    watch: {
        textValue(newValue) {
            console.log("textvalue", newValue)
        }
    }
}
</script>

<style scoped></style>