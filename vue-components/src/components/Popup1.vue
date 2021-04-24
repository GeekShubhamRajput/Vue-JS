<template>
  <div>
    <h2>Popup content</h2>
    
    <input type="text" v-model="name">
    <button @click="$emit('close', name)">Close Popup</button>
  </div>
</template>

<script>
  export default{
    name: 'Popup1',
    emits: {
      close: (name) => {
        if(!name){
          return false
        }else{
          return true
        }
      }
    },
    data(){
      return{
        name: '',
      }
    }
  }
</script>

<style></style>
