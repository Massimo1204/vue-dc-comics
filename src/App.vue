<template>
  <div id="app">
    <mainHeader />
    <mainContent />
    <mainNavigation />
  </div>
</template>

<script>
import mainHeader from "./components/header.vue";
import mainContent from "./components/content.vue";
import mainNavigation from "./components/navigation.vue";

export default {
  name: "App",
  components: {
    mainHeader,
    mainContent,
    mainNavigation,
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
