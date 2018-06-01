<template>
  <section v-if="selectedPokemon" class="viewer">
    <img :src="selectedPokemon.url_image">
    <h2 class="pokemon-name">{{ selectedPokemon.pokemon.toUpperCase() }}</h2>
    <div id="viewer-content">
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
  <section id="default-message" class="viewer" v-else>
    <h1>Select a Pokemon</h1>
    
  </section>
</template>

<script>

export default {
  props: ['selectedPokemon']
}

</script>

<style>
.viewer {
  display: grid;
  grid-template: 3fr auto 1fr / 1fr 1fr;
  grid-template-areas: 
    "picture picture"
    "name name"
    "info stats";
  margin: 30px;
  padding: 30px;
  background: greenyellow;
  border-radius: 25px;
  border: 1px solid black;
  text-align: center;

}

img {
  grid-area: picture;
  max-width: 370px;
  height: auto;
  align-content: center;
  margin: 0 auto;
}
.pokemon-name {
  grid-area: name;
  text-align: center;
  margin-bottom: 15px;
}

#default-message {
  text-align: center;
}

</style>