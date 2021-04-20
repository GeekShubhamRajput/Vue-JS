<template>
  <h2>{{title}}</h2>
  <h2>Total Likes - {{likes}}</h2>
  <h2>Published - {{isPublished ? "Yes" : "No"}}</h2>
</template>

<script>
  export default{
    name: 'Article',
    props: {
      title: {
       type: String,
       required: true,
       default: "My Default Title",  
      },
      likes: Number,
      isPublished: Boolean,
    }
  }
</script>

<style></style>