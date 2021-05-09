<template>
  <h1>Reusability with Mixins</h1>
  <ClickCounter />
  <HoverCounter />
</template>

<script>
  import HoverCounter from './components/HoverCounter.vue'
  import ClickCounter from './components/ClickCounter.vue'

  export default{
    name: 'App',
    components: {
      ClickCounter,
      HoverCounter,
    }
  }
</script>

<style>
</style>
