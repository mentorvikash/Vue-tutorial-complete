<template>
    <div class="main">
        <CardElement>Card Content 1</CardElement>
        <CardElement>
            <h1>My New Heading add text</h1>
        </CardElement>
        <CardElement>
            <img src="https://image.khaleejtimes.com/?uuid=c6164f6d-a0a6-5492-96c9-395b0455f1cf&function=cropresize&type=preview&source=false&q=75&crop_w=0.99999&crop_h=0.74971&x=0&y=0&width=1200&height=675"
                alt="Random Image" width="300" />
        </CardElement>
        <CardElement>
            <template v-slot:header>Header</template>
            <template v-slot:default>
                <img src="https://image.khaleejtimes.com/?uuid=c6164f6d-a0a6-5492-96c9-395b0455f1cf&function=cropresize&type=preview&source=false&q=75&crop_w=0.99999&crop_h=0.74971&x=0&y=0&width=1200&height=675"
                    alt="Random Image" width="300" />
            </template>
            <template v-slot:footer>
                <button>View Details</button>
            </template>
        </CardElement>
    </div>
</template>

<script>
import CardElement from './card.vue';
export default {
    name: 'SlotMain',
    components: {
        CardElement
    }
}
</script>

<style scoped>
.main {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}
</style>