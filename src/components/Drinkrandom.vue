<template>
    <div class="drink-content pt-5">
        <div class="container-lg pt-5">
            <div class="row">
                <div class="col-xs-12 col-md-6" id="drinkrandom">
                    <div v-for="(element, index) in drink" :key="index" class="card mb-3 text-center" style="max-width: 540px;"> 
                        <img :src="element.strDrinkThumb" class="img-fluid rounded-start" alt="...">                                
                        <div class="card-body">
                            <h4 class="card-title pb-3">
                                <strong>
                                    {{element.strDrink}}
                                </strong>                               
                            </h4>
                            <h4 class="card-title pb-3">
                                <strong>
                                    {{element.strCategory}}
                                </strong>   
                            </h4>
                            <h5>
                                <strong>
                                    Categoria: 
                                </strong>  
                            </h5>
                            <p class="card-text">                               
                                {{element.strCategory}}                             
                            </p>
                            <h5>
                                <strong>
                                    Bicchiere:  
                                </strong>  
                            </h5>
                            <p class="card-text">
                                {{element.strGlass}}                                
                            </p>
                            <h5>
                                <strong>
                                    Ingredienti: 
                                </strong>  
                            </h5>
                            <p class="card-text">
                                {{element.strIngredient1}}
                                <br>
                                {{element.strIngredient2}}
                                <br>
                                {{element.strIngredient3}}
                                <br>
                                {{element.strIngredient4}}
                                <br>
                                {{element.strIngredient5}}
                                <br>
                                {{element.strIngredient6}}
                                <br>
                                {{element.strIngredient7}}
                            </p>
                            <h5>
                                <strong>
                                    Ricetta: 
                                </strong>  
                            </h5>
                            <p class="card-text">
                                {{element.strInstructionsIT}}
                            </p>
                            <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
                        </div>
                    </div>
                </div>

                <div class="col-xs-12 col-md-6">
                    <h2>Un drink ad ogni refresh</h2>
                    <p class="text-light">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                        <br>
                        <br>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                        <br>
                        <br>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                        <br>
                        <br>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                        <br>
                        <br>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                        <br>
                        <br>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                        <br>
                        <br>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                        <br>
                        <br>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                        <br>
                        <br>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae quis vitae voluptatem blanditiis repudiandae deleniti sed sunt nemo similique. Nam reprehenderit magnam dicta debitis, tempore illo repudiandae ea itaque optio?
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    name: "Drinkrandom",
     data() {
        return {
            apiURL : 'https://www.thecocktaildb.com/api/json/v1/1/random.php',
            drink: [],
            // loading: true
        }
    },
    created(){
        this.randomDrink();
    },
    methods: {
        randomDrink(){
            axios
            .get(this.apiURL)
            .then (picker =>{
                // console.log(picker);
                this.drink = picker.data.drinks;
                console.log(this.drink);
            })
        }
    }

}
</script>

<style scoped lang="scss">
    .drink-content{
        background: rgb(124,145,252);
        background: linear-gradient(180deg, rgba(124,145,252,1) 0%, rgba(65,96,251,1) 50%, rgba(19,58,254,1) 100%);
        .container-lg{
            .row{
                // .col-xs-12{

                // }
            }
        }
    }
</style>