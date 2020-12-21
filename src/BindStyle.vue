<template>
  <p v-bind:style="{'font-style': fontItalic, 'font-size': 30+ 'px'}"> font sytle italic</p>
  
  <p v-bind:style="{color: 'green',
         'font-size': 20 + 'px',
         'font-weight': 'bold',}"> This is success style</p>
  
  <p v-bind:style="successStyleObject"> This is success Object style</p>
  <p v-bind:style="[successStyleObject, dangerStyleObject]"> This is override style</p>
</template>

<script>
  export default{
    name: 'BindStyle',
    data(){
      return{
        fontItalic: 'italic',
        successStyleObject: {
         color: 'green',
         'font-size': 20 + 'px',
         'font-weight': 'bold',
        },
        dangerStyleObject: {
         color: 'red',
         'font-size': 20 + 'px',
         'font-weight': 'bold',
        },
      };
    },
  };
</script>

<style>
  #app{
    text-align: center; 
  }
</style>
