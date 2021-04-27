<template>
  <h1>Component Style</h1>

  <h4>App component text</h4>
  <ComponentStyles>
    <h4>Hello Shubham</h4>
  </ComponentStyles>
</template>

<script>
  import ComponentStyles from "./components/ComponentStyles.vue"

  export default{
    name: 'App',
    components: {
      ComponentStyles,
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
  h4{
    color: orange;
  }
</style>
