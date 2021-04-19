<template>
  <h2>Volume Tracker (0-20)</h2>
  <h2>Current Volume - {{volume}} </h2>
  <button class="success" @click="volume += 2"> Increase Volume</button>
  <button class="danger" @click="volume -= 2"> Decrease Volume</button>
</template>

<script>
  export default{
    name: 'Watchers',
    data(){
      return{
        volume: 0
      }
    },
    watch: {
      volume(newVal, oldVal){
        if(newVal > oldVal && newVal === 16){
          alert('Listing to a high volume a long time may damage your hearings');
        }
      }
    }
  }
</script>

<style>
  #app{
    text-align: center;
  }
  button{
    padding: 7px;
    margin-left: 5px;
    color: white;
    font-weight: bold;
  }
  .success{
    background-color: green;
  }
  .danger{
    background-color: red;
  }
</style>
