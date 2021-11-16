<template>
  <h1>{{ title }} </h1>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: 'My Vue'
    }
  }
}
</script>

<style>
h1 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ec0e19;
  margin-top: 60px;}
</style>
