<template>
  <h2 v-once>{{ name }}</h2>
  <button @click="name='Batman'">Change name</button>
  <h2 v-pre>{{ name }}</h2>
</template>

<script>
  export default{
    name: 'BonusDirective',
    data(){
      return{
        name: 'Shubham'
      }
    }
  }
</script>

<style>
  #app{
    text-align: center;
    color: red;
  }
  button{
    padding: 7px;
    font-weight: bold;
    color: white;
    background-color: blue;
  }
</style>
