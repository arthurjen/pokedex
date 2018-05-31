<template>
  <div class="header">
    <h2>Header</h2>
    <PokeFilter/>
    <PokeSort/>

  </div>
</template>

<script>
import PokeFilter from './PokeFilter'
import PokeSort from './PokeSort'

export default {
  components: {
    PokeFilter, 
    PokeSort
  },
  props: ['filtered'] 
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
