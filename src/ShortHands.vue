<template>
  <p :class="myClass"> Short hand for Class</p>
  <button :disabled="isDisabled"> Short hand for Attribute</button>
  <p :id="myDiv"> Short hand for ID</p>
  <p :style="myStyleObject"> Short hand for Style</p>
</template>

<script>
  export default{
    data(){
      return{
        isDisabled: 'disabled',
        myClass: 'primary',
        myDiv: 'myDiv',
        myStyleObject: {'font-weight': 'bold', 'font-style': 'italic'},
      };
    },
  };
</script>

<style>
  #app{ text-align: center; font-size: 35px;}

  .primary{ color: blue }

  #myDiv{ color: orange }
</style>
