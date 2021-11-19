<template>
  <h1>{{ title }} </h1>
  <input type="text" ref="name" focus={{}}>
  <button @click="handleClick">Click me</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: 'My First Vue App!'
    }
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    }
  }
}
</script>

<style>
h1 {
  border-bottom : 1px solid #ddd;
  display: inline block;
  padding-bottom : 10 px
  }
</style>
