<template>
  <p v-for="(name, index) in names" :key="name">{{ index + 1 }} {{ name }}</p>

  <div class="fullName">
    <p v-for="fullName in fullNames" :key="fullName">{{ fullName.first }} {{ fullName.last }}</p>
  </div>

  <div class="cricketers" v-for="cricketer in cricketers" :key="cricketer.country">
    <h1> {{ cricketer.country }} </h1>
    <h3 v-for="player in cricketer.players" :key="player"> {{ player }} </h3>
  </div>

  <div class="myInfo">
    <p v-for="(value, key) in myInfo" :key="value"> {{ key }} : {{ value }} </p>
  </div>

  <template v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <hr>
  </template>
</template>


<script>
  export default{
    name: 'ListRendering',
    data(){
      return{
        names: ["Shubham", "Abhishek", "Kartik"],
        
        fullNames: [{ first: 'Shubham', last: 'Rajput'}, { first: 'Abhishek', last: 'Souner' }, { first: 'Kartik', last: 'Meena' }],
            
        cricketers: [ { country: 'India', players: ['Ms Dhoni', 'Gautam', 'Kaif'] }, { country: 'NewZeland', players: ['San Bond', 'Brendon', 'Franklin']} ],

        myInfo: { name: 'Shubham Rajput', designation: 'Sr Software Engineer', technology: 'RoR, Vue' }
      };
    },
  };
</script>

<style>
  #app{
    text-align: center;
  }
  p{
    font-size: 35px;
    font-style: bold;
  }
  div.cricketers{
    background-color: yellow;
    padding: 3px;
  }
  div.myInfo, div.fullName{
    background-color: blue;
    color: yellow;
    padding: 3px;
  }
</style>
