<template>
  <h2>Checking mounted hook</h2>
</template>

<script>
  export default{
    name: 'MyBook',
    created(){
      this.checkConsole();
    },
    data() {
      return {
        books: 0
      }
    },
    methods: {
      checkConsole(){
        console.log("In console");
      }
    }
  }
</script>

<style>
</style>
