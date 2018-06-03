<template>
  <div class="sort">
    <h2>Sort</h2>
    <input type="radio" id="id" value="id" v-model="sorted.sortBy">
    <label for="id">ID</label>
    
    <input type="radio" id="name" value="pokemon" v-model="sorted.sortBy">
    <label for="name">Name</label>
    
    <input type="radio" id="attack" value="attack" v-model="sorted.sortBy">
    <label for="attack">Attack</label>

    <input type="radio" id="defense" value="defense" v-model="sorted.sortBy">
    <label for="defense">Defense</label>
  </div>
</template>

<script>
export default {
  props: ['sorted']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
