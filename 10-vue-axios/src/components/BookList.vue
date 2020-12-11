<template>
  <div class="container">
    <button @click="load">Load books</button>
    <ul>
      <li v-for="(b, i) in books" v-bind:key="i">{{ b.title }}</li>
    </ul>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function () {
    return {
      books: [],
    };
  },
  methods: {
    load: async function () {
      let response = await axios.get(
        "https://raw.githubusercontent.com/benoitvallon/100-best-books/master/books.json"
      );
      console.log(response.data);
      this.books = response.data;
    },
  },
};
</script>

<style scoped>
</style>