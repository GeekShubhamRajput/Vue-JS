<template>
  <h1>Non Prop Attributes</h1>

  <Article1 id="my-article" title="My Article" :likes="2" :isPublished="true" />
</template>

<script>
  import Article1 from './components/Article1'

  export default {
    name: 'App',
    components: {
      Article1,
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
