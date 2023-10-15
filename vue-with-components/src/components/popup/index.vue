<template>
    <div>
        <h1>Popup Example</h1>
        <button @click="openPopup"> Open Popup </button>
        <!-- here we recieve our custom close event and trigger an callback action -->
        <PopupElement v-show="isPopupOpen" @close="onClosePopup" />
    </div>
</template> 

<script>
import PopupElement from './popupElement.vue';
export default {
    name: "PopupExample",
    data() {
        return {
            isPopupOpen: false
        }
    },
    methods: {
        openPopup() {
            this.isPopupOpen = true;
        },
        onClosePopup(name) {
            this.isPopupOpen = false;
            console.log("name: ", name)
        }
    },
    components: {
        PopupElement
    }
}
</script>

<style scoped></style>