<template>
  <div class="type-button">
    <input type="checkbox"
      :id="types"
      :value="types"
      v-model="filtered.type"
      >
    <label :for="types">{{ types.replace(/^\w/, c => c.toUpperCase()) }}</label>
  </div>
</template>

<script>

export default {
  props: ['types', 'filtered']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.type-button {
  border: 1px solid black;
  

}
input {
  display: none;
}

input:checked ~ label {
  background: darkblue;

}

label {
  cursor: pointer;
  padding-right: 10px;
  padding-left: 10px;
  background: blue;
  color: white;
}

</style>
