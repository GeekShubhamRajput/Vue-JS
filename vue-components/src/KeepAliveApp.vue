<template>
  <h1>Keeping Dynamic Components Alive</h1>
  
  <button @click="activeTab='TabA'">TabA</button>
  <button @click="activeTab='TabB'">TabB</button>
  <button @click="activeTab='TabC'">TabC</button>

  <keep-alive>
    <component :is="activeTab" />
  </keep-alive>  
</template>

<script>
  import TabA from './components/TabA'
  import TabB from './components/TabB'
  import TabC from './components/TabC'

  export default{
    name: 'App',
    components: {
      TabA, TabB, TabC,
    },
    data(){
      return{
        activeTab: 'TabA',
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
