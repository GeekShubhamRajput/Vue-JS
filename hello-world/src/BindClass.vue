<!-- 
  1. Static class
  2. Dynamic class
  3. Static and dynamic class
  4. Simple condition
  5. Ternary operator
  6. Conditional 
  7. Array
  8. Object approach
 -->

<template>
  <p class="danger"> This is Static class</p>
  <p v-bind:class="myClass"> This is Dynamic class </p>
  <p class="primary" v-bind:class="myClass"> This is Static and Dynamic classes together </p>
  <p v-bind:class="isSoldOut && 'success'"> This is conditional example </p>
  <p v-bind:class='["italicText", "success"]'> Bind array of classes </p>
  <p v-bind:class="isSoldOut ? 'primary' : 'danger'"> This is Ternary example </p>
  <p v-bind:class='[ isSoldOut && "italicText", isSoldOut ? "primary" : "danger"]'> Array with conditional </p>
  <p v-bind:class='{
    "italicText": isSoldOut , 
    "primary": isSoldOut,
    "danger": !isSoldOut,
  }'
  > Object approach </p>
</template>

<script>
  export default{
    name: 'BindClass',
    data(){
      return{
        isSoldOut: true,
        myClass: 'italicText', 
      };
    },
  }; 
</script>

<style>
  #app{ text-align: center; font-weight: bold; font-size: 40px;}
  .danger{ color: red; }
  .success{ color: green; }
  .primary{ color: blue; }
  .italicText{ font-style: italic; }
</style>
