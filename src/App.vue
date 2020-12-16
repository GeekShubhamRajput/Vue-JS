<template>
  <div> My name is {{ name }} </div>
  <div> I am {{ designation }} </div>
  <div v-html="technologies"> </div>
  <p v-html="myLink"> </p>
</template>

<script>
  export default{
    name: "App",
    data(){
      return{
        name: "Shubham Rajput",
        designation: "Software Engineer",
        technologies: '<b>Ruby on Rails</b>',
        myLink: `<a herf="#" onclick="alert('Congratulation !!')">Click here to win prize</a>`,
      };
    },
  };
</script>
