<template>
  <!-- <LetGreet name="Amar" fruit="Mango" />
  <LetGreet name="Rajat" fruit="Papaya" />
  <LetGreet name="Vishal" fruit="Orange" />
  <LetGreet :name="name" :fruit="fruit" /> -->
  <!-- <ArticleData id="articleId" tilte="What is Cat" author="Mk Rao" :likes="15" :isPublished=true /> -->
  <!-- <ComponentA /> -->
  <PopupExample />
  <InputMain />
  <!-- <SlotMain /> -->
  <!-- <SlotAdvance /> -->
  <DynamicTab />
  <TeleportMain />
</template> 

<script>
// import LetGreet from './components/greet.vue';
// import ArticleData from './components/article.vue';
// import ComponentA from './components/nestedComponet/componentA.vue';
import PopupExample from './components/popup/index.vue';
import InputMain from './components/customInput/index.vue';
// import SlotMain from './components/slots/index.vue';
// import SlotAdvance from './components/slotsAdvance/index.vue';
import DynamicTab from './components/dynamicTab/index.vue';
import TeleportMain from './components/teleport/index.vue';

export default {
  name: 'App',
  data() {
    return {
      name: 'Revive',
      fruit: 'Coding',
      default: "Artile Default Value"
    }
  },
  provide: {
    username: "Vikash Singh"
  },
  components: {
    // LetGreet,
    // ArticleData,
    // ComponentA,
    PopupExample,
    InputMain,
    // SlotMain,
    // SlotAdvance,
    DynamicTab,
    TeleportMain
  },
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