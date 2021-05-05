<template>
  <input type="text" ref="inputRef" />
  <PostIndex ref="postIndexRef" />
</template>

<script>
  import PostIndex from './PostIndex.vue'

  export default{
    name: 'TemplateRef',
    components: {
      PostIndex
    },
    mounted(){
      console.log(this.$refs.postIndexRef);
      this.$refs.inputRef.focus();
    }
  }
</script>

<style scoped>
  input:focus {
    outline: none;
    border:1px solid red;
    box-shadow: 0 0 10px #719ECE;
  }
</style>
