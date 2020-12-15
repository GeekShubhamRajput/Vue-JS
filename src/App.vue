<template>
  <p>My name is {{ name }}</p>
  <p>I am {{ age }} yr old</p>
</template>

<script>

  export default {
    name: "App",
    data(){
      return{
        name: "Shubham",
        age: 12,
      }; 
    },
  };

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
