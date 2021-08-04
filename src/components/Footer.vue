<template>
  <footer class="py-5">
    <div class="container-lg py-5">
      <div class="row">
        <div class="col-xs-12 col-md-4" v-for="(contatto, index) in contatti " :key="index">
          <h5>Contatti:</h5>
          <p>
            {{contatto.societa}}
            <br>
            {{contatto.indirizzo}}
            <br>
            {{contatto.telefono}}
          </p>
        </div>

        <div class="col-xs-12 col-md-4">
          <h5>Link utili:</h5>
          <ul>
            <li v-for="(link, index) in links" :key="index">
              <a :href="link.url">{{link.text}}</a>
            </li>
          </ul>
        </div>

        <div class="col-xs-12 col-md-4">
          <h5>Seguici sui social</h5>
          <a href="#">
            <i class="fab fa-twitter-square"></i>
            Twitter
          </a>
          <br>
          <a href="#">
            <i class="fab fa-facebook-square"></i>
            Facebook
          </a>
          <br>
          <a href="#">
            <i class="fab fa-instagram-square"></i>
            Instagram
          </a>
        </div>

      </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: "Footer",
    data(){
        return{
          contatti: [
            {
              "societa": "Cheers Srl",
              "indirizzo": "Via Blablabla 111, Milano",
              "telefono": "02 123 456 789",
            }
          ],
          links: [
            {
              text: 'link 1',
              url:'#',
              current: false
            },
            {
              text: 'link 2',
              url:'#',
              current: false
            },
            {
              text: 'link 3',
              url:'#',
              current: false
            }
          ]
        }
    }
}
</script>

<style scoped lang="scss">
  footer{
    color: white;
    background: rgb(19,58,254);
    background: linear-gradient(180deg, rgba(19,58,254,1) 0%, rgba(31,54,172,1) 50%, rgba(12,32,136,1) 100%);
    .container-lg{
      .row{
        .col-xs-12{
          color: white;
          a{
            color: white;
          }
        }
      }
    }
  }
</style>