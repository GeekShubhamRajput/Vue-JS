<template>
  <template v-for="name in names" :key="name">
    <h2 v-if="name==='Shubham'">{{name}}</h2>
  </template>
</template>

<script>
  export default{
    data(){
      return{
        names: ['Shubham', 'Kartik', 'Abhishek'],
      };
    },
  };
</script>

<style>
  #app{
    text-align: center;
    font-size: 35px;
    color: red;  
  }
</style>
