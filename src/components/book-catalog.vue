<template>
  <div class="book-catalog">
    <h1>Витрина книжного магазина</h1>
    <book-catalog-item
      v-for="book in books"
      :key="book.id"
      :book_info="book"
      @sendAddedBookId="showInConsole"
    />
  </div>
</template>

<script>
import bookCatalogItem from "./book-catalog-item.vue";

export default {
  name: "book-catalog",
  components: {
    bookCatalogItem,
  },
  props: {},
  data() {
    return {
      books: [],
    };
  },
  mounted() {
    this.fetchData()
  },
  computed: {},
  methods: {
    showInConsole(data) {
      console.log(data);
    },
    fetchData() {
      this.axios.get('http://localhost:3000/books')
      .then(response => this.books = response.data)
    },
  },
};
</script>

<style>
</style>