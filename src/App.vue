<template>
  <div id="app">

    <Header/>
    <Jumbotron/>
    <Drinklist/>
    <Chisiamo/>
    <Drinkrandom/>
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Jumbotron from "./components/Jumbotron.vue";
import Drinklist from "./components/Drinklist.vue";
import Chisiamo from "./components/Chisiamo.vue";
import Drinkrandom from "./components/Drinkrandom.vue";

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    Drinklist,
    Chisiamo,
    Drinkrandom,
  },
};
</script>

<style lang="scss">
@import '@/style/common.scss';

</style>
