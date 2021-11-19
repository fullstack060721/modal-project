<template>
  <div class="backdrop">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <h1>{{ heading }}</h1>
      <p>{{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['heading', 'text', 'theme']
}
</script>

<style>
  .modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: rgb(245, 243, 243);
    border-radius: 10px;
  } 
  
  .modal h1 {
    color: #03cfb4;
    border: none;
    padding: 0;
  }
  .modal p {
    font-style: normal;
  }
/* sale styles */
  .modal.sale {
    background: crimson;
    color: white;
  }
  .modal.sale h1 {
    color: white;
  }
  
</style>