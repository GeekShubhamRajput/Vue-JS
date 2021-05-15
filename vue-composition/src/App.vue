<template>
  <h1>Option API Data</h1>
  <Data />
  <hr />
  <ReplacingDataWithRef />
</template>

<script>
  import Data from './components/Data.vue'
  import ReplacingDataWithRef from './components/ReplacingDataWithRef.vue'

  export default {
    name: 'App',
    components: {
      Data, ReplacingDataWithRef,
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
