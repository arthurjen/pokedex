<template>
  <div class="filter">
    
    <div>
      <input type="number" placeholder="Minimum HP" v-model.number="filtered.hp"> 
    </div>
    <TypeButton 
      v-for="n in types"
      :key="n"
      :types="n"
      :filtered="filtered"
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
.filter {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  padding: 30px;
  
}

</style>
