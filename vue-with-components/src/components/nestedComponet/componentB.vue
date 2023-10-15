<template>
    <div>
        <componentC />
    </div>
</template>

<script>
import componentC from './componentC.vue';

export default {
    name: 'ComponentB',
    components: {
        componentC
    }
}
</script>

<style scoped></style>