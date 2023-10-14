<template>
  <h1>Render Conditional Items with Computed Block</h1>
  <h3 :style="{ color: 'green' }"> When ever possible we have to render a list of item we have to go with computed item
  </h3>
  <h2>Print item name price grater then 180</h2>
  <h2 :style="{ color: 'green' }">Code directly in UI</h2>
  <div v-for="item in items" :key="item.id">
    <h3 v-if="item.price > 180"> {{ item.name }} {{ item.price }}</h3>
  </div>
  <h2 :style="{ color: 'green' }">Code from computed block</h2>
  <h3 v-for=" item in filterItems" :key="item.id"> {{ item.name + " " + item.price }} </h3>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      items: [
        {
          id: 1,
          name: 'tv',
          price: 120
        },
        {
          id: 2,
          name: 'phone',
          price: 200

        },
        {
          id: 3,
          name: 'laptop',
          price: 250
        }
      ]
    }
  },
  methods: {
  },

  computed: {
    filterItems() {
      return this.items.filter(item => item.price > 180)
    }
  }

}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

.form-main {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  gap: 10px;

}

.experience-block {
  display: flex;
  gap: 5px;
}
</style>
