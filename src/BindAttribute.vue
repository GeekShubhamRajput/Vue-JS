<template>
  <div v-bind:id="myId">My name is Shubham Rajput</div>
  <div v-bind:class="myClass">I am learning Vue Js</div>
  <button v-bind:disabled="isDisabled">Click here</button>
</template>

<script>
  export default{
    name: 'BindAttribute',
    data(){
      return{
        myId: 'redFont',
        myClass: 'greenFont boldText',
        isDisabled: true,
      };
    },
  };
</script>

<style>
  #redFont{
    font-size: 25px;
    color: red;
    text-align: center;
  }
  .greenFont{
    font-size: 25px;
    color: green;
    text-align: center;
  }
</style>
