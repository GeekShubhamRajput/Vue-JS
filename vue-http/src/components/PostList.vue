<template>
  <button @click = "getPostList()"> Load Post</button>
  <h2 v-if="errorMsg" >{{ errorMsg}}</h2>
  <div v-for="post in posts" :key="post.id" >
    <h3>{{post.id}}. {{ post.title}}</h3>
    <p>{{ post.body}}</p>
    <hr />
  </div>
</template>

<script>
  import axios from 'axios'

  export default{
    name: "PostList",
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

<style></style>
