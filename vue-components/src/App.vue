<template>
  <h1>Named Slots</h1>
  
  <Card1>
    <template v-slot:header>
      <h2>Header</h2>
    </template>
    
    <template v-slot:default>
      <p>Content</p>
      <img src="https://picsum.photos/200" />
    </template>

    <template v-slot:footer>
      <h3>Footer section</h3>
    </template>
  </Card1>

</template>

<script>
  import Card1 from './components/Card1.vue'

  export default{
    name: 'App',
    components: {
      Card1,
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
