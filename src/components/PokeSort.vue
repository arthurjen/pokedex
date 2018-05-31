<template>
  <div class="sort">
    <h2>Sort</h2>
    <input v-model="sorted.sortBy">
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
