<template>
  <h2>Component C content</h2>
  <input type="text" v-model="name" />
</template>

<script>
  export default{
    name: 'TabC',
    data(){
      return{
        name: '',
      }
    }
  }
</script>

<style></style>
