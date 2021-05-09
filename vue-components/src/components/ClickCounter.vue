<template>
  <button @click="incrementCounter" >Click {{ count}} times</button>  
</template>

<script>
  import CounterMixin from '../mixins/counter'
  
  export default{
    name: 'ClickCounter',
    mixins: [CounterMixin],
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
