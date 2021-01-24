<template>
  <Greet1 name="Abhishek" heroName="Batman" />
  <Greet1 name="Kartik" heroName="Superman" />
  <Greet1 name="Sona" heroName="Wonder Woman" />
  <Greet1 :name="name" :heroName="desig" />
</template>

<script>
  import Greet1 from './components/Greet1'

  export default {
    name: 'App',
    components: {
      Greet1,
    },
    data(){
      return{
        name: 'Shreya',
        desig: 'Doctor' 
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
