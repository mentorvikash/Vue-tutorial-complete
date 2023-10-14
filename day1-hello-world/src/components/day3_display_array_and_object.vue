<template>
    <h2>diplay arrry of names</h2>
    <h3 v-for="name of names" :key="name">{{ name }}</h3>
    <h2>display array of objects</h2>
    <h3 v-for="user in users" :key="user.fname"> {{ user.fname }} {{ user.lname }} </h3>
    <h2>display object keys</h2>
    <h3 v-for="value in myFamilyInfo" :key="value">{{ value }}</h3>
    <h3 v-for="(value, key, index) in myFamilyInfo" :key="index"> {{ index + 1 }} {{ key + " " + value }}</h3>
    <h2>display nested array in object</h2>
    <div v-for="(game, index) in games" :key="index">
        <h3>{{ game.name }}</h3>
        <template v-for="player in game.players" :key="player">
            <span>{{ player }}</span>
        </template>
        <hr>
    </div>
    <h2>Condition render only specific element of array</h2>
    <div v-for=" (user, index) in usersList" :key="index">
        <h3 v-if="user === 'madhuri'">{{ user }}</h3>
    </div>
</template>
  
<script>
export default {
    name: "App",
    data() {
        return {
            names: ["vikash", "rajat", "vishal"],
            users: [
                {
                    fname: "vikash",
                    lname: "singh"
                },
                {
                    fname: "revived",
                    lname: "coding"
                }

            ],
            myFamilyInfo: {
                user1: "vikash singh",
                user2: "rajat singh",
                user3: "vishal singh"
            },
            games: [
                {
                    name: "cricket",
                    players: ["sachine", "ms dhoni"]
                },
                {
                    name: "kabadi",
                    players: ["anit thapa", "gaza maldo"]
                }
            ],
            usersList: ["riya", "priya", "madhuri"]
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
</style>
  