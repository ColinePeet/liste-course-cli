<template>
    <div id="container" >
      <div class="alert ingredient" :class="{'alert-info':!isSelected,'alert-success':isSelected}">
        <i :click="toggle(ingredient)" :class="{'fa-check-square':isSelected}" class="fa fa-square"></i>     
          {{ingredient}}
        <button @click="deleteItem(index)" class="bouton">
          <img src="https://png.pngtree.com/svg/20161008/the_trash_40525.png" alt="">
        </button> 
      </div>
    </div>
</template>

<script>
export default {
  props: ['ingredient', 'isSelected'],

  computed:{
    	ingredientsSelected(){
      	let selected = this.list.filter(i => i.isSelected);
        let selectedNames = selected.map(i => i.ingredient);
        return selectedNames.join(' ');
      }
    },

  methods:{
    toggle(i){
    	i.isSelected = !i.isSelected;
    },
    // ajouter:function(){
    // 	this.list.push({ingredient:this.newIngredient, isSelected:false})
    //   this.newIngredient= null;
    // },
    // deleteItem(index){
    // 	this.list.splice(index, 1);
    // }
  }

}
</script>

<style>

</style>
