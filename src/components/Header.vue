<template>
    <header>

    <nav>
        <!-- start container -->
        <div class="container-lg">
            <!-- start row -->
            <div class="row">
                <!-- start logo -->
                <div class="col-2 col-md-2">
                    <img src="/img/logo.jpg" alt="logo cheers" class="logo-header">
                </div>
                <!-- end logo -->

                <!-- start link -->
                <div class="col-10 pt-5">  
                    <ul>
                        <li v-for="(link, index) in link" :key="index" class="px-5"> 
                            <a :href="link.url">{{link.text}}</a>
                            <div class="col-2">
                                <ul v-if="link.subitems"> 
                                    <li v-for="(page, index) in link.subitems" :key="index">
                                        <a class="dropdown" :href="page.url">
                                            {{page.text}}
                                        </a>    
                                    </li>
                                </ul>                            
                            </div>    
                        </li>
                    </ul>

                </div>
                <!-- end link -->
            </div>
            <!-- end row -->
        </div>
        <!-- end container -->
    </nav>

</header>
</template>

<script>
export default {
    name: "Header",
    data (){
    return {
        link :[
        {
          text: 'Home',
          url:'#',
          current: false,
            subitems:[
            {
            text: 'Link',
            url:'#',
            current: false,          
            },
            {
            text: 'Link',
            url:'#',
            current: false
            },
            {
            text: 'Link',
            url:'#',
            current: false
            }              
            ]
        },
        {
          text: 'I nostri drink',
          url:'#drink',
          current: false,
            subitems:[
            {
            text: 'Link',
            url:'#',
            current: false,
            },
            {
            text: 'Link',
            url:'#',
            current: false
            },
            {
            text: 'Link',
            url:'#',
            current: false
            }              
            ]
        },
        {
          text: 'Chi siamo',
          url:'#chisiamo',
          current: false,
          subitems:[
            {
            text: 'Link',
            url:'#',
            current: false,
          
            },
            {
            text: 'Link',
            url:'#',
            current: false
            },
            {
            text: 'Link',
            url:'#',
            current: false
            }              
            ]
        },
        {
          text: 'DrinkRandom',
          url:'#drinkrandom',
          current: false,
          subitems:[
            {
            text: 'Link',
            url:'#',
            current: false,
          
            },
            {
            text: 'Link',
            url:'#',
            current: false
            },
            {
            text: 'Link',
            url:'#',
            current: false
            }              
            ]
        },
        {
          text: 'Contatti',
          url:'#contatti',
          current: false,
          subitems:[
            {
            text: 'Link',
            url:'#',
            current: false,
          
            },
            {
            text: 'Link',
            url:'#',
            current: false
            },
            {
            text: 'Link',
            url:'#',
            current: false
            }              
            ]
        }
        ]
    }
  }
}
</script>

<style scoped lang="scss">
    header{
        background-color: #972939;
        nav{
            .container-lg{
                .row{
                    .col-2{
                        .logo-header{
                            height: 130px;
                            object-fit: cover;
                        }
                    }
                    .col-10{
                        ul{
                            // height: 110px;
                            // line-height: 110px;
                            li{
                                display: inline-block;
                                list-style: none;
                                font-size: 14px;   
                                    &:hover .dropdown{
                                            color: white;
                                    }
                                    a{
                                        color: white;
                                        text-decoration: none;
                                    }
                                    ul{
                                        padding: 0;
                                        li{
                                            .dropdown{
                                                color: transparent;
                                                &:hover{
                                                    color: white;
                                                    
                                                }
                                            }                                           
                                        }
                                    }
                            }
                        }
                    }
                }
            }
        }
    }
</style>