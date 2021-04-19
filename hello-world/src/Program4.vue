<template>
  <template v-for="item in items" :key="item.id">
    <h2 v-if="item.price > 150"> {{item.name}} {{item.price}}</h2>
  </template>
  <hr>
  <h1>Using computed property</h1>
  <h2 v-for="item in expensiveItem" :key="item.id"> {{item.name}} {{item.price}}</h2>
</template>

<script>
  export default{
    name: 'Program4',
    data(){
      return{
        items: [
          {id: 1, name: 'TV', price: 100},
          {id: 2, name: 'Mobile', price: 150},
          {id: 3, name: 'Lapy', price: 200},
          {id: 4, name: 'IPad', price: 250}
        ]
      }
    },
    computed: {
      expensiveItem(){
        return this.items.filter( item => item.price > 150 );
      }
    }
  }
</script>

<style>
  #app{ text-align: center; }
</style>
