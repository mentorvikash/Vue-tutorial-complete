<template>
  <h1>Getter and Setter</h1>
  <h2>Non-Computed fullName {{ fname }} {{ lname }}</h2>
  <h2>Computed fullName {{ fullName }}</h2>
  <button @click="setfullName">Change Name</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      fname: "revive",
      lname: "codiing",
    }
  },
  methods: {
    // trigger this method -> Computed fullName trigger -> set fucntion to set new fname and lname.
    setfullName() {
      this.fullName = "vikash singh"
    }
  },

  computed: {
    fullName: {
      get() {
        const fullname = this.fname + " " + this.lname
        return fullname
      },
      set(value) {
        const nameArray = value.split(" ");
        this.fname = nameArray[0]
        this.lname = nameArray[1]
      }
    },
    totalPrice() {
      const total = this.items.reduce((total, current) => (total + current.price), 0)
      return total
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
