<template>
  <h2>In component A</h2>
  <ComponentB />
</template>

<script>
  import ComponentB from './ComponentB'

  export default{
    name: 'ComponentA',
    components: {
      ComponentB,
    },
    data(){
      return{
        
      }
    }
  }
</script>

<style></style>
