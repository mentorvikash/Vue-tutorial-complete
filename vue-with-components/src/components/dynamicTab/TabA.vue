<template>
    <div>
        <h3>Tab A Content</h3>
        <input text v-model="fname" placeholder="frist name" />
    </div>
</template>

<script>
export default {
    name: 'TabA',
    data() {
        return {
            fname: ""
        }
    }
}
</script>

<style scoped></style>