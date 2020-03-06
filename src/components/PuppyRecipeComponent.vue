<template>
        <div class="card">
          <div class="row no-gutters">
           <div class="col-sm-4">
               <img class="card-img" :src="recipe_img" alt="recipe image">
            </div>
               <div class="col-sm-8">
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
  name: 'PuppyRecipeComponent',
  props: ["recipe_img", "title", "ingredients", "website"]

}
</script>


<style scoped>
    
    img {
        
        padding: 25px 10px 10px 10px;
        border-radius: 10px;
        
    }
    
    .card {
        
        margin: 10px;
    }

</style>
