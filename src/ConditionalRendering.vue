<template>
  <p v-if="num===0">Number is zero</p>
  <p v-else-if="num > 0">Number is Positive</p>
  <p v-else-if="num < 0">Number is Negative</p>
  <p v-else>This is not a number</p>

  <div v-if="display">
    <p>My name is Shubham Rajput</p>
  </div>
</template>

<script>
  export default{ 
    data(){
      return{
        num: 1,
        display: true,
      }
    }
  }
</script>

<style>
  #app{
    text-align: center;
    font-size: 35px;
  }
</style>
