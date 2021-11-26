<template>
    <div class="result">
        <p>Reaction time - {{ score }} ms </p>
        <p>{{ rank }}</p>
    </div>
</template>

<script>
export default ({
    props: ['score'],
    data() {
        return  {
            rank: null
        }
    },
    mounted() {
        if (this.score < 500) {
            this.rank = "Ninja fingers !"
        }
        else {
            this.rank = "you can do better ..."
        }
    }
})
</script>

<style>
  .result {
    width: 200px;
    border-radius: 20px;
    background:  #c9c509;
    color: white;
    text-align: center;
    padding: 1px 0;
    margin: 40px auto;
  }
</style>