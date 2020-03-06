<template>
    
    <div class="card">
        <div v-for="recipe in recipes" class="col-sm-4" :key="recipe.title">
            
            <PuppyRecipeComponent
                
                    :recipe_img = "recipe.thumbnail"
                    :title = "recipe.title"
                    :ingredients = "recipe.ingredients"
                    :website = "recipe.href"
                
            ></PuppyRecipeComponent>
            
        </div>
    </div>
    
</template>


<script>

    import PuppyRecipeComponent from "./components/PuppyRecipeComponent.vue"
    
    export default {
        
        name: "PuppyRecipePage",
        components: {
            PuppyRecipeComponent
        },
        
        data() { 
            return { 
                recipes: [] 
            }
        },
    
        created() {
            
            const app = this;
            
            const corsUrl = "https://cors-anywhere.herokuapp.com/";
            const url = "http://www.recipepuppy.com/api/";

           fetch(corsUrl + url)
            .then(response => response.json())
            .then((res) => {
               
                app.recipes = res.results
               //console.log(app.recipes)
               
            })
        }
    }
    
</script>