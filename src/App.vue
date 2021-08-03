<template>
  <div id="app">

    <Header/>
    <Jumbotron/>
    <Drinklist/>
    <Chisiamo/>
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

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    Drinklist,
    Chisiamo,
  },
};
</script>

<style lang="scss">
@import '@/style/common.scss';

</style>
