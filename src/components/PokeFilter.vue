<template>
  <div class="filter">
    
    <div>
      <input type="number" v-model.number="filtered.hp"> 
    </div>
    <TypeButton 
      v-for="n in types"
      :key="n"
      :types="n" 
      @select="filterByType"/> 
  </div>
</template>

<script>
import TypeButton from './TypeButton';

export default {
  data() {
    return {
      filterBy: [],
    }
  },
  props: ['filtered', 'types'],
  components: {
    TypeButton
  },
  methods: {
    filterByType(types) {
      this.filtered.type = types;     
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
