<template>
    <div class="drink-content pt-5">
        <div class="container-lg pt-5">
            <div class="row">
                <div class="col-xs-12">
                    <h2 id="drinkrandom" class="text-center py-5">Un drink ad ogni refresh</h2>
                </div>
            </div>
            <div class="row">
                <div class="col-xs-12 col-md-4">
                    <div v-for="(element, index) in drink" :key="index" class="card mb-3 text-center mx-auto" style="max-width: 540px;"> 
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
                        </div>
                    </div>
                </div>

                <div class="col-xs-12 col-md-4">
                    <div v-for="(element, index) in drink2" :key="index" class="card mb-3 text-center mx-auto" style="max-width: 540px;"> 
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
                        </div>
                    </div>
                </div>

                <div class="col-xs-12 col-md-4">
                    <div v-for="(element, index) in drink3" :key="index" class="card mb-3 text-center mx-auto" style="max-width: 540px;"> 
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
                        </div>
                    </div>
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
            drink2: [],
            drink3: [],
            // loading: true
        }
    },
    created(){
        this.randomDrink();
        this.randomDrinkDue();
        this.randomDrinkTre();
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
        },
        randomDrinkDue(){
            axios
            .get(this.apiURL)
            .then (picker =>{
                // console.log(picker);
                this.drink2 = picker.data.drinks;
                console.log(this.drink2);
            })
        },
        randomDrinkTre(){
            axios
            .get(this.apiURL)
            .then (picker =>{
                // console.log(picker);
                this.drink3 = picker.data.drinks;
                console.log(this.drink3);
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
                .col-xs-12{
                    .card{
                        background-color: transparent;
                        color: white;
                        border: none;
                    }
                }
            }
        }
    }
</style>