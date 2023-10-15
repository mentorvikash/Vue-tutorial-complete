<template>
    <div>
        <h1>Component A</h1>
        <ComponentB />
    </div>
</template>

<script>
import ComponentB from './componentB.vue';
export default {
    name: 'ComponentA',
    components: {
        ComponentB
    }
}
</script>

<style scoped></style>