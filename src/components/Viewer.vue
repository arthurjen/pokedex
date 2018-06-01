<template>
  <section v-if="selectedPokemon" class="viewer">
    <img :src="selectedPokemon.url_image">
    <div id="viewer-content">
      <p>Name: {{ selectedPokemon.pokemon }}</p>
      <p>Type: {{ selectedPokemon.type_1 }} <span v-if="selectedPokemon.type_2 !== 'NA'">and {{ selectedPokemon.type_2 }}</span></p>
      <p>Height: {{ selectedPokemon.height * 10 }} centimeters</p>
      <p>Weight: {{ selectedPokemon.weight }}</p>


    </div>
  </section>
  <section v-else>
    
  </section>
</template>

<script>

export default {
  props: ['selectedPokemon']
}

</script>

<style>
.viewer {
  background: greenyellow;
  border-radius: 25px;
  border: 1px solid black;
}
</style>