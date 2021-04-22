<template>
  <h1>Provide and Inject</h1>
  <h2> App component username - {{ name}} </h2> 
  <ComponentA />
</template>

<script>
  import ComponentA from './components/ComponentA'

  export default {
    name: 'App',
    components: {
      ComponentA,
    },
    data(){
      return{
        name: 'Shubham Rajput',
      }
    },
    provide(){
      return{
        username: this.name,
      } 
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
</style>
