<template>
  <div>
    <form @submit.prevent="createPost()">
      <div>
        <label for="userId">UserId </label>
        <input type="text" v-model="formData.userId" />
      </div>
      <div>
        <label for="title">Title</label>
        <input type="text" v-model="formData.title" />
      </div>
      <div>
        <label for="body">Body</label>
        <textarea v-model="formData.body" />
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
  import axios from 'axios'

  export default{
    name: "CreatePost",
    data(){
      return{
        formData: {
          userId: '',
          title: '',
          body: '',
        }
      }
    },
    methods: {
      createPost(){
        axios.post('https://jsonplaceholder.typicode.com/posts', this.formData)
          .then(response => console.log(response))
          .catch(error => console.log(error))
      }
    }
  }
</script>

<style>
</style>

