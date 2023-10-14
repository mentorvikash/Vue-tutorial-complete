<template>
    <h1>Computed Value vs Methord</h1>
    <h3>Here we had used 4 Modifire .trim .age .number and .prevent</h3>
    <div>
        <pre>
      {{ JSON.stringify(formData, null, 2) }}
    </pre>
    </div>
    <form class="form-main" @submit.prevent="handleFormSubmit">
        <div>
            <label for="name">Name: </label>
            <input type="text" id="name" v-model.trim="formData.name">
        </div>
        <div>
            <label for="email">Email: </label>
            <input type="text" id="email" v-model="formData.email">
        </div>

        <div>
            <label for="profile">Profile Summery: </label>
            <textarea id="profile" v-model.lazy="formData.profileSummery" />
        </div>
        <div>
            <label for="country">Select Country</label>
            <select id="country" v-model="formData.country">
                <option value="">---select your country---</option>
                <option value="India">India</option>
                <option value="United Kingdom">United Kingdom</option>
                <option value="United State">United State</option>
            </select>
        </div>
        <div>
            <label for="job-location">Select Job Location</label>
            <select id="job-location" multiple v-model="formData.jobLocation">
                <option value="India">India</option>
                <option value="Germary">Germary</option>
                <option value="United State">United State</option>
                <option value="Japan">Japan</option>
                <option value="United Kingdom">United Kingdom</option>
            </select>
        </div>
        <div>
            <label for="remote-work">Romote Location: </label>
            <input type="checkbox" id="remote-work" v-model="formData.remoteLocation" true-value="Yes" false-value="No">
        </div>

        <div>
            <label><b>Skills: </b></label>
            <input type="checkbox" id="html" value="html" v-model="formData.skills" />
            <label for="html">HTML</label>
            <input type="checkbox" id="css" value="css" v-model="formData.skills" />
            <label for="css">CSS</label>
            <input type="checkbox" id="javascript" value="javascript" v-model="formData.skills" />
            <label for="javascript"> Javascript </label>
            <input type="checkbox" id="vue" value="vue.js" v-model="formData.skills" />
            <label for="vue"> Vue </label>
        </div>

        <div class="experience-block">
            <label><b>Years of experience: </b></label>
            <input type="radio" id="0-1" value="0-1" v-model="formData.experienceYear">
            <label for="0-1">0-1</label>
            <input type="radio" id="2-6" value="2-6" v-model="formData.experienceYear">
            <label for="2-6">2-6</label>
            <input type="radio" id="6+" value="6+" v-model="formData.experienceYear">
            <label for="6+"> 6+ </label>
        </div>

        <h4 :style="{ color: 'green' }"> Note: Here when you enter your age and hit enter your from get submitted</h4>
        <div>
            <label for="age">Age: </label>
            <input @keyup.enter="handleFormSubmit" type="number" id="age" v-model.number="formData.age">
        </div>
        <h4 :style="{ color: 'green' }">Note: Bounus Directive</h4>
        <!-- <button type="submit">Submit</button> -->
    </form>
    <div v-once>
        <h3 v-pre>here we had use v-pre tag {{ staticText }}</h3>
        <h3>{{ staticText }}</h3>
        <button v-on:click="staticText = 'rajat singh'">change button</button>
    </div>
</template>
  
<script>
export default {
    name: "App",
    data() {
        return {
            formData: {
                name: "",
                email: "",
                profileSummery: "",
                country: "",
                jobLocation: [],
                remoteLocation: 'No',
                skills: [],
                experienceYear: "",
                age: null,
            },
            staticText: "vikash singh"
        }
    },
    methods: {
        handleFormSubmit() {
            console.log("fromvalues", this.formData);
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
  