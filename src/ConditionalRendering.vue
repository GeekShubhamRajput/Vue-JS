<template>
  <p v-if="num===0">Number is zero</p>
  <p v-else-if="num > 0">Number is Positive</p>
  <p v-else-if="num < 0">Number is Negative</p>
  <p v-else>This is not a number</p>
  <p v-if="display">My name is Shubham Rajput</p>
  
  <p v-if="isDisplay">Displaying this element using v-if redirective</p>
  <p v-show="isDisplay">Displaying this element using v-show redirective</p>

</template>

<script>
  export default{ 
    data(){
      return{
        num: 1,
        display: true,
        isDisplay: false,
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
