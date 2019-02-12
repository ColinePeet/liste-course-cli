<template>
    <div>
        <Ingredient v-for="(i, index) in list" :key="index" :ingredient="i.ingredient" :selected="i.isSelected" />
    </div>
</template>

<script>
import Ingredient from './Ingredient.vue'

export default {
    data (){
        return {
            list:[{ingredient:"courgette",isSelected:false},{ingredient:"champignon",isSelected:false},{ingredient:"bananes",isSelected:false}],
            newIngredient: null,
        }
    },
    components: {
        Ingredient
    }
}
</script>

<style>

</style>

