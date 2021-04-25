<template>
  <div id="header" >
    <slot name="header"></slot>
  </div>

  <div id="content" >
    <slot></slot>
  </div>

  <div id="footer" >
    <slot name="footer"></slot>
  </div>
</template>

<script>
  export default{
    name: 'Card1',
  }
</script>

<style></style>
