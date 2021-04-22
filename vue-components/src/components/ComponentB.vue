<template>
  <h2>In component B</h2>

  <ComponentC />
</template>

<script>
  import ComponentC from './ComponentC'

  export default{
    name: 'ComponentB',
    components: {
      ComponentC,
    },
  }
</script>

<style></style>
