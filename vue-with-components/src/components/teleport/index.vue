<template>
    <teleport to="#teleport-block">
        <TeleportComponent />
    </teleport>
    <button @click="openModel">Open Model</button>
    <teleport to="#teleport-model">
        <TeleportModel v-if="isModelOpen" @close="closeModel" />
    </teleport>
</template>

<script>
import TeleportComponent from './teleportComponent.vue';
import TeleportModel from './teleportModel.vue';
export default {
    name: 'TeleportMain',
    data() {
        return {
            isModelOpen: false,
        }
    },
    components: {
        TeleportComponent,
        TeleportModel
    },
    methods: {
        openModel() {
            this.isModelOpen = true;
        },
        closeModel() {
            this.isModelOpen = false;
        }
    }
}
</script>

<style scoped></style>