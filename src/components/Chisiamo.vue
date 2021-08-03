<template>
    <div class="info">
        <div class="container-lg">
            <div class="row">
                <div class="col-12 text-center">
                    <h2 id="chisiamo">Chi siamo</h2>
                </div>
            </div>
            <div class="row">
                <div class="col-xs-12 col-md-6 p-5">
                    <h3 class="pb-3">Il nostro Staff</h3>
                    <p>
                        <strong>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!
                            <br>
                            <br>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!
                            <br>
                            <br>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!
                            <br>
                            <br>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!
                            <br>
                            <br>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!
                            <br>
                            <br>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!
                            <br>
                            <br>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!
                            <br>
                            <br>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!
                        </strong>
                    </p>
                </div>

                <div class="col-xs-12 col-md-6 mt-5">

                    <VueSlickCarousel v-bind="settings" :slidesToScroll="2" :slidesToShow="2" :vertical="true" :swipeToSlide="true">
                        <div class="box-card" v-for="(persona, index) in personale" :key="index">
                            <div class="card" style="max-width: 540px;">
                                <img :src="persona.img" :alt="persona.alt"> 
                                <div class="card-body text-center">
                                    <h5 class="card-title">
                                        <strong>
                                        {{persona.nome}}
                                        </strong>
                                    </h5>
                                    <h5 class="card-title">
                                        <strong>
                                        {{persona.mansione}}
                                        </strong>
                                    </h5>
                                    <p class="card-text">{{persona.descrizione}}</p>
                                </div>                                
                            </div>
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
    name: "Chisiamo",
    components: { VueSlickCarousel },
    data(){
        return{
            personale: [
                {
                    "nome": "Fra",
                    "mansione": "Barman - Alchimista",
                    "descrizione": "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!",
                    "img": "/img/fra.png",
                    "alt": "Barman Cheers",
                },
                {
                    "nome": "Matteo",
                    "mansione": "Degustatore seriale",
                    "descrizione": "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!",
                    "img": "/img/Matteo.png",
                    "alt": "Degustatore Cheers",
                },
                {
                    "nome": "Nicolò",
                    "mansione": "Animazione",
                    "descrizione": "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!",
                    "img": "/img/nico.png",
                    "alt": "Animazione Cheers",
                },
                {
                    "nome": "Bob",
                    "mansione": "Buttafuori",
                    "descrizione": "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum asperiores officia qui. Iusto animi aliquam adipisci itaque veritatis nisi vel, dolorum hic harum. Pariatur vitae iure iusto architecto fuga. Nobis!",
                    "img": "/img/bob.png",
                    "alt": "Sicurezza Cheers",
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    .info{
        background: rgb(226,136,214);
        background: linear-gradient(180deg, rgba(226,136,214,1) 0%, rgba(231,184,224,1) 50%, rgba(124,145,252,1) 100%);
        .container-lg{
            .row{
                .col-xs-12{
                    p{
                        color: white;
                    }
                }
            }

            .row{
                .col-xs-12{
                    .box-card{
                        .card{
                            h5{
                                font-size: 25px;
                            }
                            p{
                                color: black;
                            }
                            img{
                                height: 300px;
                                object-fit: cover;
                            }
                        }
                    }
                }
            }
        }
    }
</style>