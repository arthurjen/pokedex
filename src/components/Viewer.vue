<template>
  <section v-if="selectedPokemon" class="viewer">
    <img :src="selectedPokemon.url_image">
    <div id="viewer-content">
      <p>Name: {{ selectedPokemon.pokemon }}</p>
      <p>Type: {{ selectedPokemon.type_1 }} <span v-if="selectedPokemon.type_2 !== 'NA'">and {{ selectedPokemon.type_2 }}</span></p>
      <p>Height: {{ selectedPokemon.height / 10 }} m</p>
      <p>Weight: {{ selectedPokemon.weight / 10 }} kg</p>
    </div>
    <div id="viewer-stats">
      <p>HP: {{ selectedPokemon.hp }}</p>
      <p>Speed: {{ selectedPokemon.speed }}</p>
      <p>Attack: {{ selectedPokemon.attack }}</p>
      <p>Defense: {{ selectedPokemon.defense }}</p>
      <p>SP. Att.: {{ selectedPokemon.special_attack }}</p>
      <p>SP. Def.: {{ selectedPokemon.special_defense }}</p>
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
  
  flex-direction: column;
  align-items: center;
  margin: 30px;
  padding: 30px;
  background: greenyellow;
  border-radius: 25px;
  border: 1px solid black;
}

img {
  max-width: 100%;
  height: auto;
}
</style>