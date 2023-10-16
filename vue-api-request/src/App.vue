<template>
  <h1>Api Request in Vue</h1>
  <AllPost />
  <PostRequest />
</template>

<script>

import AllPost from "./components/getRequest/index.vue"
import PostRequest from "./components/postRequest/index.vue"

export default {
  name: 'App',
  components: {
    AllPost,
    PostRequest
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<!-- first install some package to make api request, we are using axios -->