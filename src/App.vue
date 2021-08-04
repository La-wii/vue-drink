<template>
  <div id="app">

    <Header/>
    <Jumbotron/>
    <Drinklist/>
    <Chisiamo/>
    <Drinkrandom/>
    <Footer/>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Jumbotron from "./components/Jumbotron.vue";
import Drinklist from "./components/Drinklist.vue";
import Chisiamo from "./components/Chisiamo.vue";
import Drinkrandom from "./components/Drinkrandom.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    Drinklist,
    Chisiamo,
    Drinkrandom,
    Footer,
  },
};
</script>

<style lang="scss">
@import '@/style/common.scss';

</style>
