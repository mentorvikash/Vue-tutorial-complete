<template>
    <div class="main">
        <UsersElement>
            <template v-slot:default="slotProps">
                <h1> {{ slotProps.lastName }} {{ slotProps.firstName }}</h1>
            </template>
        </UsersElement>
        <UsersElement>
            <template v-slot:default="slotProps">
                <h1> {{ slotProps.firstName }} {{ slotProps.lastName }}</h1>
            </template>
        </UsersElement>
        <UsersElement>
            <template v-slot:default="slotProps">
                <h1>{{ slotProps.firstName }}</h1>
            </template>
        </UsersElement>
    </div>
</template>

<script>
import UsersElement from './users.vue';
export default {
    name: 'SlotMain',
    components: {
        UsersElement
    }
}
</script>

<style scoped>
.main {
    /* display: flex; */
    /* flex-direction: column; */
}
</style>