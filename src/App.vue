<template>
  <div id="app">

    <h1>Pokedex</h1>
    <PokeHeader :filtered="filter"/>
    <Results :pokeList="pokemonList"/>


  </div>
</template>

<script>

import PokeHeader from './components/PokeHeader';
import Results from './components/Results';
import pokemonList from '../pokemon.js';

export default {
  data() {
    return {
      pokemonList: pokemonList,
      filter: {
        type: ''

      }
    }

  },
  components: {
    PokeHeader,
    Results

  }
}
</script>

<style>

</style>
