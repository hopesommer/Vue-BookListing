<template>
  <form class="" action="#" method="post">
    <input v-model="bookTitle" type="text" name="title" value="" placeholder="Book Title">
    <input v-model="bookAuthor" type="text" name="author" value="" placeholder="Book Author">
    <button type="submit" v-on:submit.prevent="bookSubmit(bookTitle, bookAuthor)" name="button">Add Book</button>
  </form>

</template>

<script>
  export default {
    name: 'BookForm',
    props: ['books'],
    methods: {
      bookSubmit(bookTitle, bookAuthor) {
        this.$emit('addBook', bookTitle, bookAuthor)
      }
    },
    data() {
      return {
        bookTitle: '',
        bookAuthor: '',
      }
    }
  }

</script>

<style>

</style>
