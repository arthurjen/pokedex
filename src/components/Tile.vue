<template>
  <div class="tile" :style="{ background: pokemon.color_1}">
    <div>
      <img :src="pokemon.url_image">
      <p>{{ pokemon.pokemon }}</p>
      <p>Attack: {{ pokemon.attack }}</p>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      
    }
  },
  props: ['pokemon']
}




</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tile {
  width: 150px;
  height: 150px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 5px;
  padding: 10px;
  transition: all 1s ease;
  border: 1px solid white;
  border-radius: 8px;
}


img {
  width: 100px;
}
</style>
