<template>
  <div class="results">
    <Tile 
      v-for="pokemon in pokeList"
      :key="pokemon.id"
      :pokemon="pokemon"
      />

  </div>
</template>

<script>
import Tile from './Tile'


export default {
  components: {
    Tile

  },

  props: ['pokeList']
  
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.results {
  display: flex;
  flex-wrap: wrap;
}
</style>
