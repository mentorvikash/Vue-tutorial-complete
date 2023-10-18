<template>
    <TargetRefChild v-model="inputvalue" />
</template>

<script>
import TargetRefChild from "./targetRefChild.vue"

export default {
    name: "RefMain",
    components: {
        TargetRefChild
    },
}
</script>

<style scoped></style>