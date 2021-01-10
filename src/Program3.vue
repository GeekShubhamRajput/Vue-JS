<template>
  <h2>Has Books: {{hasBooks}}</h2>
</template>

<script>
  export default{
    name: 'ComputedProperty',
    data(){
      return{
        authorBook: {
          author: 'Shubham',
          books: [
            'Alchemist', 'The Heror', 'KingMan'
          ]
        }
      }
    },
    computed: {
      hasBooks(){
        return this.authorBook.books.length > 0 ? 'Yes' : 'No';
      }
    }
  }
</script>

<style>
  #app{
    text-align: center;
    color: blue;
  }
</style>
