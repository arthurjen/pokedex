<template>
  <div class="filter">
    <h2>Filter</h2>
    <input v-model="filtered.type">
  </div>
</template>

<script>
export default {
  props: ['filtered']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
