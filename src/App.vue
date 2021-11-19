<template>
  <h1> {{ title }} </h1>
  <p>Welcome ... </p>
  <Modal :heading="heading" :text="text" theme="sale"/>
  <Modal :heading="heading" :text="text" theme="no sale"/>
</template>

<script>

import Modal from './components/Modal.vue'

export default {
  name: 'App',
  data() {
    return {
      title: 'My first Vue app!',
      heading: 'Sign up for the Giveaway',
      text: 'Grab your swag for half price'
    }
  },
  components: {
    Modal
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
