<template>
  <h2>In component C username - {{username}}</h2>
</template>

<script>
  export default{
    name: 'ComponentC',
    inject: ['username']
  }
</script>

<style></style>
