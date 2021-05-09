<template>
  <h2 @mouseover = "incrementCounter" >Hover mouse {{ count}} times</h2>
</template>

<script>
  import CounterMixin from '../mixins/counter'  

  export default{
    name: 'HoverCounter',
    mixins: [CounterMixin],
  }
</script>

<style></style>