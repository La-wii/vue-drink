<template>
    <div class="drink-content pt-5">
        <div class="container-lg pt-5">
            <div class="row">
                <div class="col-xs-12 col-md-6">
                    <div v-for="(element, index) in drink" :key="index" class="card mb-3" style="max-width: 540px;"> 
                        <img :src="element.strDrinkThumb" class="img-fluid rounded-start" alt="...">                                
                        <div class="card-body">
                            <h4 class="card-title pb-3">{{element.strCategory}}</h4>
                            <p class="card-text">                               
                                <span>Categoria: </span>
                                <br>
                                {{element.strCategory}}                             
                            </p>
                            <p class="card-text">
                                <span>Bicchiere: </span> 
                                <br>
                                {{element.strGlass}}                                
                            </p>
                            <p class="card-text">
                                <span>Ingredienti: </span>
                                <br>
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
                            <p class="card-text">
                                <span>Ricetta: </span> {{element.strInstructionsIT}}
                            </p>
                            <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
                        </div>
                    </div>
                </div>

                <div class="col-xs-12 col-md-6">
                    <h2>Un drink ad ogni refresh</h2>
                    <p>
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