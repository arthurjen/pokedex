<template>
  <div id="app">

    <h1>Pokedex</h1>
    <p>{{ filter.type }}</p>
    <p>{{ sort.sortBy }}</p>
    <p>{{ pokeList }}</p>
    <PokeHeader :filtered="filter" :sorted="sort"/>
    <Results :pokeList="filterPokemon"/>

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
      },
      sort: {
        sortBy: ''
      },
      pokeList: []
    }

  },
  computed: {
    filterPokemon() {
      return this.pokemonList
        .slice()
        .sort((a, b) => a.attack - b.attack)
      
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
