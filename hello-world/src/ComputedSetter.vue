<template>
  <h2> Fullname - {{firstName}} {{lastName}}</h2>
  <hr />
  <h1> FullName using Computed Property</h1>
  <h2>{{fullName}}</h2>
  <button @click="changedFullname()"> Change name</button>
</template>

<script>
  export default{
    name: 'ComputedSetter',
    data(){
      return{
        firstName: 'Shubham',
        lastName: 'Rajput'
      }
    },
    methods: {
      changedFullname(){
        this.fullName = 'Abhishek Souner';
      }
    },
    computed: {
      fullName: {
        get(){
          return `${this.firstName} ${this.lastName}`;  
        },
        set(value){
          const names = value.split(' ');
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
    color: white;
    background-color: blue;
  }
</style>
