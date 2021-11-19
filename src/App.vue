<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>

  <div v-if="showModal">
    <Modal :heading="heading" :text="text" theme="sale" @close="toggleModal" />
    <!-- <Modal :heading="heading" :text="text" theme="sale" v-on:close="toggleModal" /> -->
    <!-- <Modal :heading="heading" :text="text" theme="sale" v-on:my-event="toggleModal" /> -->
  </div>  
  <button @click="toggleModal">open modal</button>

</template>

<script>
// emitter(string, function ...)
// emitter('close', this.toggleModal)
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
#app {
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