<template>
  <div> My name is {{ name }} </div>
  <div> I am {{ designation }} </div>
  <div v-text="technologies"> </div>
</template>

<script>

  export default{
    name: "App",
    data(){
      return{
        name: "Shubham Rajput",
        designation: "Software Engineer",
        technologies: 'Ruby on Rails',
      };
    },
  };

</script>
