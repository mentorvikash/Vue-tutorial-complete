<template>
    <div v-for="user in users" :key="user.name">
        <slot :firstName="user.fname" :lastName="user.lname"></slot>
    </div>
</template>

<script>
export default {
    name: 'UsersElement',
    data() {
        return {
            users: [
                {
                    fname: "vikash",
                    lname: "singh"
                },
                {
                    fname: "rajat",
                    lname: "singh"
                },
                {
                    fname: "vishal",
                    lname: "singh"
                }
            ],
        }
    }
}
</script>

<style scoped></style>