<template>
  <div id="app">
    <bookMainWrapper/>
  </div>
</template>

<script>
import bookMainWrapper from "./components/book-main-wrapper.vue"
export default {
  name: 'App',
  components: {
   bookMainWrapper
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
