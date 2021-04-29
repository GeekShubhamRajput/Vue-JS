<template>
  <h2>Teleport Component</h2>

  <teleport to="#teleported">
    <TeleportComponent />
  </teleport>
</template>

<script>
  import TeleportComponent from './components/TeleportComponent'

  export default{
    name: 'App',
    components: {
      TeleportComponent,
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
