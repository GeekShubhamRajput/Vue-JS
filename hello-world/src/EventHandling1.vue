<template>
  <h2>{{ name }}</h2>
  <h2>{{ count }}</h2>
  <div>
    <button class="success" @click="increment(), changeName()">Increment 1</button>
    <button class="danger" @mouseover="decrement($event)">Decrement 1</button>
  </div>
</template>

<script>
  export default{
    name: 'EventHandling1',
    data(){
      return{
        name: 'Shubham',
        count: 0,
      }
    },
    methods: {
      changeName(){
        this.name = 'Vijay';
      },
      increment(){
        this.count += 1;
      },
      decrement(event){
        this.count -= 1;
        console.log('Event', event);
      },
    },
  };
</script>

<style>
  #app{
    text-align: center;
  }
  button{
    padding: 7px;
    color: white;
    margin-left: 5px;
  }
  .success{
    background-color: green;
  }
  .danger{
    background-color: red;
  }
</style>
