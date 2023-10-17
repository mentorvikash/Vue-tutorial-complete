<template>
    <!-- <button @click="getPost">Get All Post</button> -->
    <div v-if="error" :style="{ color: 'red' }">{{ error }}</div>
    <div v-for="post in allPost" :key="post.id">
        <h2>{{ post.title }}</h2>
        <h4>{{ post.body }}</h4>
        <hr />
    </div>
</template>

<script>
import axios from "axios"

export default {
    name: 'AllPost',
    created() {
        // this created block will trigger on component mount once
        this.getPost();
    },
    data() {
        return {
            allPost: [],
            error: ""
        }
    },
    methods: {
        getPost() {
            axios.get('https://jsonplaceholder.typicode.com/posts?limit=20')
                .then(response => this.allPost = response.data)
                .catch(error => this.error = error.message)
        }
    }

}
</script>

<style scoped></style>