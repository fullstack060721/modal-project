<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>

  <!-- <div v-if="showModal"> -->
  <teleport to="#modals" v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <p>{{ title }}</p>        
        <a href="#">Sign Up now</a>
        <a href="#">More Info</a>
      </template>
    </Modal>
  </teleport>  

  <button @click.alt="toggleModal">open modal</button>

</template>

<script>

import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
  data() {
    return {
      title: 'My First Vue App!',

      heading: 'Sign up for the Giveaway!',
      text: 'Grab your swag for half price!',

      showModal: false,
    }
  },
    methods: {
    toggleModal() {
      this.showModal = !this.showModal
    }
  }
}
</script>

<style>
#app, #modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
