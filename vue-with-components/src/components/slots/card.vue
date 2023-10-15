<template>
    <div class="card-main">
        <div id="card-header">
            <slot name="header"></slot>
        </div>
        <div id="card-body">
            <slot></slot>
        </div>
        <div id="card-footer">
            <slot name="footer"></slot>
        </div>
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