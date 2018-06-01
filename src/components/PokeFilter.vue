<template>
  <div class="filter">
    <h2>Filter</h2>
    <button @click="filterByNormal">normal</button>
    <button @click="filterByType">water</button>
    
  </div>
</template>

<script>
import Element from './Element';

export default {
  data() {
    return {
      elementList: ['water', 'fire', 'grass']
    }
  },
  props: ['filtered'],
  components: {
    Element
  },
  methods: {
    filterByWater() {
      this.filtered.type = 'water';
    },
    filterByNormal() {
      this.filtered.type = 'normal';
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
