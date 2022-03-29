<template>
  <div id="app">
    <indexHeader />
    <mainContent />
    <mainNav />
    <indexFooter />
  </div>
</template>

<script>
import indexHeader from "./components/Header.vue";
import mainContent from "./components/Content.vue";
import mainNav from "./components/Main.vue";
import indexFooter from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    indexHeader,
    mainContent,
    mainNav,
    indexFooter,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
