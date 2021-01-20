<template>
  <div>
    <input type="text" v-model="name" >
  </div>
  <div>
    <input type="text" v-model="movieInfo.title" >
    <input type="text" v-model="movieInfo.actor" >
  </div>
  <div>
    <button @click="movieList.push('Kabir')">Add a movie</button>
  </div>
</template>

<script>
  export default{
    name: 'Watchers',
    data(){
      return{
        name: 'Shubham',
        movieInfo: {
          title: '',
          actor: ''
        },
        movieList: ['KGF', 'Rawan']
      }
    },
    watch: {
      name: {
        handler(newVal){
          console.log(`Calling API with name = ${newVal}`)
        },
        immediate: true,
      },
      movieInfo: {
        handler(newVal){
          console.log(`Calling API with movieName = ${newVal.title} and Actor = ${newVal.actor}`)
        },
        deep: true
      },
      movieList: {
        handler(newVal){
          console.log(`Calling API with movieName = ${newVal}`)
        },
        deep: true
      }
    }
  }
</script>

<style>
  #app{
    text-align: center;
  }
  div{
    margin-top: 5px;
  }
  input{
    margin-left: 5px;
  }
  button{
    padding: 7px;
    font-size: bold;
  }
</style>
