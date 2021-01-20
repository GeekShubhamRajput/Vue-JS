<template>
  <h2 v-on:mouseover="name='Vijay'" v-on:mouseout="name='Shubham'">{{ name }}</h2>
  <div>
    <h2>{{ count }}</h2>
  </div>

  <div>
    <button class="success" v-on:click="increment(1)">Increment 1</button>
    <button class="success" v-on:click="increment(5)">Increment 5</button>
    <button class="danger" v-on:click="decrement(1)">Decrement 1</button>
    <button class="danger" v-on:click="decrement(5)">Decrement 5</button>
  </div>
</template>

<script>
  export default{
    name: 'EventHandling',
    data(){
      return{
        name: 'Shubham',
        count: 0,
      };
    },
    methods: {
      increment(num){
        return this.count += num;
      },
      decrement(num){
        return this.count -= num;
      }
    }
  };
</script>

<style>
  #app{
    text-align: center;
  }
  button{
    margin-left: 5px;
    padding: 5px;
    font-weight: bold;
    color: white;
  }
  .danger{
    background-color: red;
  }
  .success{
    background-color: green;
  }
</style>
