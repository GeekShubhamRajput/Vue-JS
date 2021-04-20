<template>
  <h1>Prop types and Validations</h1>

  <Article title="My Article" :likes="2" :isPublished="true" />
</template>

<script>
  import Article from './components/Article'

  export default {
    name: 'App',
    components: {
      Article,
    },
    data(){
      return{
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
