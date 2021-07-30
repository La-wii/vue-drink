<template>
    <header>

    <nav>
        <!-- start container -->
        <div class="container-lg">
            <!-- start row -->
            <div class="row">
                <!-- start logo -->
                <div class="col-2 pt-3">
                    <h1>LOGO</h1>
                </div>
                <!-- end logo -->

                <!-- start link -->
                <div class="col-10">  
                    <ul>
                        <li v-for="(link, index) in link" :key="index" class="ps-5"> 
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
          text: 'Chi siamo',
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
          text: 'Contatti',
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
          text: 'Blog',
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
          text: 'Shop',
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
        }
        ]
    }
  }
}
</script>

<style scoped lang="scss">
    header{
        nav{
            .container-lg{
                .row{
                    // .col-2{
                        
                    // }
                    .col-10{
                        ul{
                            
                            li{
                                display: inline-block;
                                list-style: none;
                                font-size: 14px;   
                                    &:hover .dropdown{
                                            color: black;
                                            background-color: white;
                                    }
                                    a{
                                        color: black;
                                        text-decoration: none;
                                    }
                                    ul{
                                        padding: 0;
                                        li{
                                            .dropdown{
                                                color: transparent;
                                                &:hover{
                                                    color: black;
                                                    
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