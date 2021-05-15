<template>
  <h2>Option - {{ o_firstName}} </h2>
  <h2>Composition - {{ c_firstName}} </h2>
  <h2>Composition - {{ greet}} </h2>
</template>

<script>
  import { ref} from 'vue'

  export default{
    name: "ReplacingDataWithRef",
    setup(){
      const c_firstName = ref("Abhishek")
      c_firstName.value = "Kartik"

      const greet = `Hello ${c_firstName.value}`

      return{
        c_firstName, greet
      }
    },
    data(){
      return{
        o_firstName: "Shubham",
      }
    }
  }
</script>

<style>
</style>
