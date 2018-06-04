<template>
  <div class="sort">
    <section id="first" class="section">
    <h2>Sort By:</h2>
    <div class="container">
    <input type="radio" id="id" value="id" v-model="sorted.sortBy">
    <label for="id"><span class="radio">ID</span></label>
    </div>

    <div class="container">
    <input type="radio" id="name" value="pokemon" v-model="sorted.sortBy">
    <label for="name"><span class="radio">Name</span></label>
    </div>

    <div class="container">
    <input type="radio" id="attack" value="attack" v-model="sorted.sortBy">
    <label for="attack"><span class="radio">Attack</span></label>
    
</div>

    <div class="container">
    <input type="radio" id="defense" value="defense" v-model="sorted.sortBy">
    <label for="defense"><span class="radio">Defense</span></label>
    <span id="slider"></span>
    </div>
    </section>

  </div>
</template>

<script>
export default {
  props: ['sorted']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.section input[type="radio"] {
  display: none;
  border: 2px solid orange;
}
.section {
  padding: 100px;
  padding-left: 100px;
}

.container label {
  position: relative;
  font-size: 26px;
  
}

.container span::before,
.container span::after {
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
}

.container span.radio:hover {
  cursor: pointer;
}
.container span.radio::before {
  left: -72px;
  width: 65px;
  height: 40px;
  background-color: black;
  border-radius: 50px;
  border: 2px solid orange;
  
}
.container span.radio::after {
  left: -66px;
  width: 25px;
  height: 25px;
  border-radius: 15px;
  border: 2px solid orange;
  background-color: blue;
  transition: left .25s, background-color .25s;
 
}
input[type="radio"]:checked + label span.radio::after {
  left: -38px;
  background-color: #EBFF43;
}

</style>