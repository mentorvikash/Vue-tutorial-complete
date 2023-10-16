<template>
    <form @submit.prevent="creatPost">
        <div>
            <label for="id"></label>
            <input type="number" name="" id="id" v-model="newPost.userId">
        </div>
        <div>
            <label for="title"></label>
            <input type="text" name="title" id="title" v-model="newPost.title">
        </div>
        <div>
            <label for="body"></label>
            <input type="text" name="" id="body" v-model="newPost.body">
        </div>
        <button type="submit">submit</button>
    </form>
</template>

<script>
import axios from 'axios';

export default {
    name: 'CreatePost',
    data() {
        return {
            newPost: {
                title: '',
                body: '',
                userId: null,
            }
        }
    },
    methods: {
        creatPost() {
            axios.post('https://jsonplaceholder.typicode.com/posts', this.newPost)
                .then(response => console.log(response))
                .catch(err => console.log(err.message))
        }
    }
}
</script>

<style scoped></style>