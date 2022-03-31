<template>
  <div id="app">
    <indexHeader />
    <mainJumbotron />
    <mainContent />
    <mainNavigation />
    <indexFooter />
  </div>
</template>

<script>
import indexHeader from "./components/Header.vue";
import mainContent from "./components/Content.vue";
import mainNavigation from "./components/Main.vue";
import indexFooter from "./components/Footer.vue";
import mainJumbotron from "./components/Jumbotron.vue";

export default {
  name: "App",
  components: {
    indexHeader,
    mainContent,
    mainNavigation,
    indexFooter,
    mainJumbotron,
  },
};
</script>

<style lang="scss">
@import "./components/style.scss";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
}
</style>
