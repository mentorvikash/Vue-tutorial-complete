<template>
    <div>
        <h1>Component C</h1>
        <h2>This username: {{ username }} get by provide and inject </h2>
    </div>
</template>

<script>
export default {
    name: 'ComponentC',
    inject: ['username']
}
</script>

<style scoped></style>