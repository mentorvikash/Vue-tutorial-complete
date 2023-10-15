<template>
    <div class="card-main">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'CardElement'
}
</script>

<style scoped>
.card-main {
    border: 0 solid black;
    min-width: 200px;
    box-shadow: 2px 4px 8px darkgrey;
    padding: 10px;
    max-width: 300px;
    font-size: 18px;
    font-weight: 600;

    &:hover {
        box-shadow: 1px 1px 3px darkgrey;
    }
}
</style>