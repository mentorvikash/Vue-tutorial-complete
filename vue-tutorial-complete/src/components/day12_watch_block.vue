<template>
    <h1>Watch: A way to watch a value and trigger some action at specific condition</h1>
    <h2>Volume Tracker App</h2>
    <div class="watcher-app-main">
        <h3>{{ volume }}</h3>
        <div>
            <button @click="volume -= 2">Decrease</button>
            <button @click=" volume += 2">Increase</button>
        </div>
        <div>
            <h2>Hit Api Whem movie data change</h2>
            <div>
                <label for="movie-name">Movie Name</label>
                <input type="text" id="movie-name" v-model="movieinfo.name" />
            </div>
            <div>
                <label for="writer-name">Writer Name</label>
                <input type="text" id="writer-name" v-model="movieinfo.writer.name" />
            </div>

            <div>
                <label for="movie-name">Movie Name</label>
                <input type="text" id="movie-name" v-model="movieinfo.name" />
            </div>
        </div>
        <div>
            <button @click="fruitList.push('papaya')">Add New Fruit</button>
        </div>

    </div>
</template>
  
<script>
export default {
    name: "App",
    data() {
        return {
            volume: 0,
            movieinfo: {
                name: "batman",
                writer: {
                    name: "AK Aggrawal",
                    domain: ["drama", "comedy", "romance"]
                }
            },
            fruitList: ["apple", "orange", "banana"]
        }
    },
    methods: {},

    computed: {},
    watch: {
        // Name to the watch fucntion is same as that of variable to track
        volume(newvalue, oldvalue) {
            if (newvalue > oldvalue && newvalue == 14) {
                alert("Listing to high volume for long may damage your ears")
            }
        },
        movieinfo: {
            handler(newvalue) {
                if (newvalue) {
                    console.log("name: " + this.movieinfo.name + ", writer: " + this.movieinfo.writer.name + " work with " + this.movieinfo.writer.domain.join(','))
                }
            },
            immediate: true,
            deep: true,
        },
        fruitList: {
            handler(newvalue) {
                console.log(`list of all fruit we have: ${newvalue.join(',')}`)
            },
            deep: true,
        }
    }
}

</script>
  
<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
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
  