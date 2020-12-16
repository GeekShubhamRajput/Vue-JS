<template>
  <div v-html="technologies"> </div>
  <p v-html="myLink"> </p>
</template>

<script>
  export default{
    name: "BindHtml",
    data(){
      return{
        technologies: '<b>Ruby on Rails</b>',
        myLink: `<a herf="#" onclick="alert('Congratulation !!')">Click here to win prize</a>`,
      };
    },
  };
</script>
