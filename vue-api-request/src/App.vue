<template>
  <h1>Api Request in Vue</h1>
  <!-- <AllPost /> -->
  <!-- <PostRequest /> -->
  <ResuableCode />
  <RefMain />
</template>

<script>

// import AllPost from "./components/getRequest/index.vue"
// import PostRequest from "./components/postRequest/index.vue"
import ResuableCode from "./components/resuableCode/index.vue"
import RefMain from "./components/templetRef/index.vue"
export default {
  name: 'App',
  components: {
    // AllPost,
    // PostRequest,
    ResuableCode,
    RefMain
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