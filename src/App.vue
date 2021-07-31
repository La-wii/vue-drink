<template>
  <div id="app">

    <Header/>
    <Drinklist/>
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Drinklist from "./components/Drinklist.vue";

export default {
  name: "App",
  components: {
    Header,
    Drinklist,
  },
};
</script>

<style lang="scss">
@import '@/style/common.scss';

</style>
