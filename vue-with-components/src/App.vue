<template>
  <!-- <LetGreet name="Amar" fruit="Mango" />
  <LetGreet name="Rajat" fruit="Papaya" />
  <LetGreet name="Vishal" fruit="Orange" />
  <LetGreet :name="name" :fruit="fruit" /> -->
  <ArticleData tilte="What is Cat" author="Mk Rao" :likes="15" :isPublished=true />
</template>

<script>
// import LetGreet from './components/greet.vue';
import ArticleData from './components/article.vue'

export default {
  name: 'App',
  data() {
    return {
      name: 'Revive',
      fruit: 'Coding',
      default: "Artile Default Value"
    }
  },
  components: {
    // LetGreet,
    ArticleData
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
