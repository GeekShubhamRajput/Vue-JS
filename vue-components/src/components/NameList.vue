<template>
  <div v-for="name in fullNames" :key="name.firstName">
    <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
  </div>
</template>

<script>
  export default{
    name: 'NameList',
    data(){
      return{
        fullNames: [
          { firstName: 'Shubham', lastName: 'Rajput'},
          { firstName: 'Kartik', lastName: 'Meena'},
          { firstName: 'Abhishek', lastName: 'Souner' }
        ]
      }
    }
  }
</script>

<style></style>
