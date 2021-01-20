<template>
  <div>
    <p>{{ message }}</p>
    <button v-on:click="reverseMessage">Reverse Message</button>
  </div>
</template>

<script>
  export default{
    name: 'Programe1',
    data(){
      return {
        message: 'Hello Shubham !!'
      }
    },
    methods: {
      reverseMessage(){
        this.message = this.message.split('').reverse().join('');
      },
    },
  }
</script>

<style>
  #app{ 
    text-align: center;
    font-size: 35px;
    color: red;
  }
  button{
    background-color: blue;
    padding: 5px;
  }
</style>
