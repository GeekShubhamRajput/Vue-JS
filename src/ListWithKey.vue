<template>
  <template v-for="name in names" :key="name">
    <h2>{{name}}</h2>
    <input placeholder="Enter your last name">
    <hr>
  </template>

  <button @click="shuffle">Shuffle!</button>
</template>

<script>
  import _ from "lodash";

  export default{
    name: 'ListWithKey',
    data(){
      return{
        names: ['Shubham', 'Abhishek', 'Kartik'],
      };
    },
    methods: {
      shuffle() {
        console.log(this.names);
        this.names = _.shuffle(this.names);
      },
    },
  };
</script>

<style>
  #app{
    text-align: center;
  }
  button{
    padding: 10px 20px;
    font-size: 17px;
    background-color: blue;
    color: white;
  }
</style>
