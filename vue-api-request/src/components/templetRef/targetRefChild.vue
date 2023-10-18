<template>
    <div>
        <input ref="inputRef" type="text" v-model="inputvalue">
    </div>
    <AllPost ref="childRef" />
</template>

<script>
import AllPost from '../getRequest/getAllPost.vue';

export default {
    name: 'TargetRefChild',
    data() {
        return {
            inputvalue: ""
        }
    },
    mounted() {
        console.log(" input ref", this.$refs.inputRef)
        console.log(" child ref", this.$refs.childRef)
        this.$refs.inputRef.focus();
    },
    components: {
        AllPost
    },
    updated() {
        console.log(" input value", this.$refs.inputRef.value)
    }
}
</script>

<style scoped></style>