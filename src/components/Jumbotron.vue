<template>
    <div class="jumbotron d-none d-sm-none d-md-none d-lg-block">
        <div class="container-lg">
            <div class="row">
                <div class="col-12">
                    <VueSlickCarousel v-bind="settings" :autoplay="true" :infinite="true">
                        <div class="slide" v-for="(slide, index) in slider" :key="index">
                            <img :src="slide.img" alt="">
                        </div>
                    </VueSlickCarousel>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    name: "Jumbotron",
    components: { VueSlickCarousel },
    data(){
        return{
            slider: [
                {
                    "img": "/img/1.jpg",
                },
                {
                    "img": "/img/2.jpg",
                },
                {
                    "img": "/img/3.jpg",
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    .jumbotron{
        height: 600px;
        background-color: #972939;
        .container-lg{
            height: 600px;
            .row{
                .col-12{
                    .slide{
                        img{
                           height: 600px;
                           width: 100%;
                        }
                    }
                }
            }
        }
    }
</style>