<template>
    <button @click="$emit('select', types)">{{ types }}</button>

</template>

<script>

export default {
  props: ['types']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
