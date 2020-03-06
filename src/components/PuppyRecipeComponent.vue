<template>
     <div class="card">
        <div class="row">
           <div class="col-sm-12">
               <img class="card-img-top" :src="recipe_img" :alt="recipe image">
               <div class="card-body">
                   <h3 class="card-title">{{ title }}</h3>
                   <p class="card-text">{{ ingredients }}</p>
                   <a :href="website" target="_blank">More Info</a>
               </div>
           </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Recipes',
  props: ["recipe_img", "title", "ingredients", "website"]

}
</script>


<style scoped>

</style>
