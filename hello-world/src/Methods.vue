<template>
  <h2>Multiplication method - {{ 2 * 3 }}</h2>
  <h2>Multiplication method - {{ multiply(5) }}</h2>

  <h2>Addition method - {{ 2 + 3 }}</h2>
  <h2>Addition method - {{ addition(2, 3, 5) }}</h2>
</template>

<script>
  export default{
    name: 'Methods',
    data(){
      return{
        baseMultiplier: 10,
      };
    },
    methods: {
      multiply(num){
        return num * this.baseMultiplier;
      },

      addition(a, b, c){
        return a + b + c;
      }
    }
  };
</script>

<style>
  #app{
    text-align: center;
    font-size: 30px;
    color: red;
  }
</style>
