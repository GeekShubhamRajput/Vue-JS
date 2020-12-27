<template>
  <template v-for="name in names" :key="name">
    <h2 v-if="name==='Shubham'">{{name}}</h2>
  </template>

  <template v-for="count in counting" :key="count">
    <h2 v-if="count > 2">{{count}}</h2>
  </template>
</template>

<script>
  export default{
    data(){
      return{
        names: ['Shubham', 'Kartik', 'Abhishek'],
        counting: [1, 2, 3, 4, 5, 6], 
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
