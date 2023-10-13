<template>
    <h1> {{ greet }} {{ name }}</h1>
    <p v-text="channel"></p>
    <h3 v-html="htmlContent"></h3>
    <!-- class binding -->
    <h4 class="underline success"> Underline Text</h4>
    <!-- conditional class -->
    <h3 v-bind:class="isPromoted && 'promoted'">Conditional Classes</h3>
    <!-- ternary operator -->
    <h3 v-bind:class="isSoldOut ? 'sold-out' : 'new'">Ternery Operator for sold out or new</h3>
    <!-- Apply class by array means muliple Classes -->
    <h3 v-bind:class="['promoted', 'new']">Apply class by array means muliple Classes</h3>
    <!-- Appy array of class with conditional rendering -->
    <h3 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">Appy array of class with conditional
      rendering</h3>
    <h3 v-bind:class="{ new: !isSoldOut, promoted: isPromoted, 'sold-out': isSoldOut }">Apply classes by folow object
      binding
      approach</h3>
    <h3 v-bind:style="{ color: graycolor, fontSize: '28px', 'background-color': 'orange' }">Inline style with vue</h3>
    <h3 v-bind:style="customStyling">Apply object styling</h3>
    <h3 v-bind:style="[baseStyle, extraStyle]">Apply multiple object style with Array </h3>
    <h3 :class="shortHand">The short hand syntex: we can replace v-bind with : only</h3>
  </template>
  
  <script>
  export default {
    name: "App",
    data() {
      return {
        greet: "Hello",
        name: "vikash",
        channel: "revive coding",
        htmlContent: "<b><i>here I am adding h3 tag</i></b>",
        isPromoted: true,
        isSoldOut: false,
        graycolor: 'grey',
        customStyling: {
          color: "white",
          fontSize: '24px',
          'background-color': 'black',
        },
        baseStyle: {
          padding: '5px',
          fontSize: '22px'
        },
        extraStyle: {
          border: '1px solid black',
          fontStyle: 'italic',
        },
        shortHand: {
          color: "green",
          fontWeight: 'bold',
        }
      };
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
  
  .underline {
    text-decoration: underline;
  }
  
  .success {
    color: green
  }
  
  .promoted {
    font-style: italic;
  }
  
  .new {
    color: orchid
  }
  
  .sold-out {
    color: red;
  }
  </style>
  