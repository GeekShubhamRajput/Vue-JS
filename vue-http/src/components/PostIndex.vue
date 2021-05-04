<template>
  <h3 v-if="errorMsg">{{errorMsg}}</h3>
  <div v-for="post in posts" :key="post.id">
    <h3>{{ post.id}}. {{ post.title}}</h3>
    <p>{{ post.body}}</p>
  </div>
</template>

<script>
  import axios from 'axios'

  export default{
    name: 'PostIndex',
    created(){
      this.getPostList();
    },
    data(){
      return{
        posts: [],
        errorMsg: '',
      }
    },
    methods: {
      getPostList(){
        axios.get('https://jsonplaceholder.typicode.com/posts')
        .then((response) => {
          return this.posts = response.data;
        }).catch((error) => {
          console.log(error)
          return this.errorMsg = "Something went wrong..."
        })
      }
    }
  }
</script>

<style>
</style>
