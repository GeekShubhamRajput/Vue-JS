<template>
  <h2>Addition of 6 and 2 - {{ addition(6, 2) }} </h2>
  <h2>Substraction of 2 from 6 - {{ substraction(6, 2) }} </h2>
  <h2>Multiplication of 6 and 2 - {{ multiplication(6, 2) }}</h2>
  <h2>Devision of 6 and 2 - {{ devision(6, 2) }}</h2>
  <h2>Multiplication using data attribute - {{ multiplyUsingBase(6) }}</h2>
</template>

<script>
  export default{
    name: 'Program2',
    data(){
      return{
        baseMultiplier: 10,
      }
    },
    methods: {
      addition(a, b){
        return a + b;
      },
      substraction(a, b){
        return a - b;
      },
      multiplication(a, b){
        return a * b;
      },
      devision(a, b){
        return a / b;
      },
      multiplyUsingBase(a){
        return a * this.baseMultiplier;
      },
    },
  };
</script>

<style>
  #app{
    text-align: center;
    color: blue;
  }
</style>
