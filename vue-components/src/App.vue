<template>
  <h1>Slots Props</h1>

  <NameList v-slot:default="slotProps">
    <h2>{{ slotProps.firstName}}</h2>
  </NameList>
  <hr>
  <NameList v-slot:default="slotProps">
    <h2>{{ slotProps.firstName}} {{ slotProps.lastName}}</h2>
  </NameList>
  <hr>
  <NameList v-slot:default="slotProps">
    <h2>{{ slotProps.lastName}}, {{ slotProps.firstName}} </h2>
  </NameList>
</template>

<script>
  import NameList from './components/NameList.vue'

  export default{
    name: "App",
    components: {
      NameList,
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
