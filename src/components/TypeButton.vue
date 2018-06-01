<template>
  <div>
    <input type="checkbox"
      :id="types"
      :value="types"
      v-model="filtered.type"
      >
    <label :for="types">{{ types }}</label>
  </div>
</template>

<script>

export default {
  props: ['types', 'filtered']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
