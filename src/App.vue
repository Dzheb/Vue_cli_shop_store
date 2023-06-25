<template>
  <div id="app">
    <BlogDetails />
  </div>
</template>

<script>
import BlogDetails from './components/BlogDetails.vue';


export default {
  name: 'App',
  components: {
    BlogDetails,
  
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
