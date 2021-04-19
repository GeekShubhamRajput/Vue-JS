<template>
  <h2>FullName - {{firstName}} {{lastName}}</h2>
  <h2>Computed FullName - {{ fullName }}</h2>
  
  <button @click = "items.push({id: 4, name: 'Computer', price: 100})" >Add item</button>
  <h2>Computed Total - {{ itemTotal }} </h2>
</template>

<script>
  export default{
    name: 'ComputedProperties',
    data(){
      return{
        firstName: 'Shubham',
        lastName: 'Rajput',
        
        items: [
          { id: 1,
            name: 'TV',
            price: 100
          },
          {
            id: 2,
            name: 'Laptop',
            price: 300
          }
        ]
      }
    },
    computed: {
      fullName(){
        return this.firstName + " " + this.lastName;
      },
      itemTotal(){
        return this.items.reduce((total, curr) =>(total += curr.price), 0);
      }
    }
  }
</script>

<style> 
  #app{
    text-align: center;
    color: blue;
  }
  button{
    padding: 7px;
    background-color: green;
    font-weight: bold;
    color: white;
  }
</style>
