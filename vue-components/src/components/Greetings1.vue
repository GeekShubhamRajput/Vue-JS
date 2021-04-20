<template>
  <h2>{{ name}} a.k.a. {{ heroName}}</h2>
</template>

<script>
  export default{
    name: 'Greetings',
    props: ['name', 'heroName']
  }
</script>

<style>
</style>
