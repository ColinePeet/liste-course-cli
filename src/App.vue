<template>

  <div id="app" class="col">
    <h2>
      Liste de courses
    </h2>
    <IngredientsContainer/>

    <!-- <form class="form-inline">
      <div class="form-group">
        <div class="input-group">
          <input type="text" class="form-control" v-model="newIngredient" id="new-item-field"       
          placeholder="Produit">
        </div>
      </div>
      <button @click.prevent="ajouter()" class="btn">Ajouter</button>
    </form> -->

    <!-- <div class="a-acheter">
        {{ingredientsSelected}}
    </div> -->
  </div>

</template>

<script>
import IngredientsContainer from './components/IngredientsContainer.vue'

export default {
  name: 'app',
  components: {
    IngredientsContainer,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
