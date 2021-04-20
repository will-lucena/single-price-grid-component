<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <home />
  </div>
</template>

<script>
//import HelloWorld from "./components/HelloWorld.vue";
import Home from "./views/Home.vue";

export default {
  name: "App",
  components: {
    //HelloWorld,
    Home,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/styles.scss";
@import "./assets/scss/base.scss";
</style>
