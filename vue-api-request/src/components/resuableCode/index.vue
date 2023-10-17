<template>
    <CounterBtn />
    <CountHover />
</template>

<script>
import CounterBtn from './counterBtn.vue';
import CountHover from './countHover.vue';

export default {
    name: 'ResuableCode',
    components: {
        CounterBtn,
        CountHover
    }
}
</script>

<style scoped></style>