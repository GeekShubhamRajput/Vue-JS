<template>
  <h2>Computed Item Total - {{ itemTotal}} </h2>
  <h2>Method Item Total - {{getItemTotal()}} </h2>

  <div>
    <input v-model="country">
  </div>
</template>

<script>
  export default{
    name: 'ComputedPropertyVsMethod',
    data(){
      return{
        country: '',
        items: [
          {
            name: 'TV',
            price: 200
          },
          {
            name: 'Mobile',
            price: 200
          }
        ]
      }
    },
    methods: {
      getItemTotal(){
        console.log("Item total Method");
        return this.items.reduce((total, curr)=> ( total += curr.price), 0);
      }
    },
    computed: {
      itemTotal(){
        console.log("Computed Item total");
        return this.items.reduce((total, curr)=> ( total += curr.price), 0);
      }      
    }
  }
</script>

<style>
  #app{
    text-align: center;
    color: blue;
  }
</style>
