<template>
  <h2>{{firstName}} {{lastName}}</h2>
  <button @click="changedFullName()">Change FullName</button>
  <hr />
  <h2>Using computed property :- {{fullName}}</h2>
</template>

<script>
  export default{
    name: 'ComputedSetter',
    data(){
      return{
        firstName: "Shubham",
        lastName: "Rajput"
      }
    },
    methods: {
      changedFullName(){
        this.fullName = 'Abhishek Rai';
      }
    },
    computed: {
      fullName: {
        get(){
          return this.firstName + ' ' + this.lastName;
        },
        set(newVal){
          const names = newVal.split(' ');
          this.firstName = names[0];
          this.lastName = names[1];
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
    background-color: blue;
    color: white;
  }
</style>
