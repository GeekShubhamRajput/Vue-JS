<template>
  <h1>Dynamic Components</h1>

  <button @click="activeTab = 'TabA'">Tab A</button>
  <button @click="activeTab = 'TabB'">Tab B</button>
  <button @click="activeTab = 'TabC'">Tab C</button>

  <component :is="activeTab" />
</template>

<script>
  import TabA from './components/TabA'
  import TabB from './components/TabB'
  import TabC from './components/TabC'

  export default{
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
