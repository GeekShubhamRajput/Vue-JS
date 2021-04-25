<template>
  <h1>Slots and Default Slots</h1>

  <Card></Card>
  <Card> Card Content</Card>
  <Card><b>Card Content</b></Card>
  <Card><img src="https://picsum.photos/200"></Card>
</template>

<script>
  import Card from './components/Card.vue'

  export default{
    name: 'App',
    components: {
      Card,
    },
    methods: {
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
