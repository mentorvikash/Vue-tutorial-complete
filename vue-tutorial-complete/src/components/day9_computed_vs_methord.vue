<template>
    <h1>Computed Vs Methords</h1>
    <h2>Non-Computed fullName {{ fname }} {{ lname }}</h2>
    <h2>Computed fullName {{ fullName }}</h2>
    <h2>Non-Computed Price {{ items.reduce((total, current) => (total + current.price), 0) }}</h2>
    <h3 :style="{ color: 'green' }">Computed Value gives ability to caculate once and use the same value at multiple
        places</h3>
    <h2>Compute Total Price {{ totalPrice }}</h2>
    <h3>Let say we have a button on its click we add new item to items array</h3>
    <button @click="addItem">Add Item</button>
    <h3 :style="{ color: 'green' }">methord render every time when any state change while computed use cached data</h3>
    <h2>Method fullName {{ fullNameM() }}</h2>
</template>
  
<script>
export default {
    name: "App",
    data() {
        return {
            fname: "revive",
            lname: "codiing",
            items: [
                {
                    id: 1,
                    name: 'tv',
                    price: 120
                },
                {
                    id: 2,
                    name: 'phone',
                    price: 50

                },
                {
                    id: 3,
                    name: 'laptop',
                    price: 70

                }
            ]
        }
    },
    methods: {
        addItem() {
            const obj = {
                id: 4,
                name: 'bottel',
                price: 17
            }
            this.items.push(obj);
        },
        fullNameM() {
            console.log("method block render")
            return this.fname + " " + this.lname
        }
    },

    computed: {
        fullName() {
            console.log("computed block render")
            const fullname = this.fname + " " + this.lname
            return fullname
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
  