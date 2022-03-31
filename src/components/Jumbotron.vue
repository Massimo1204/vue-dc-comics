<template>
  <div class="my-jumbo">
    <div class="abs-text">
      <h1 class="text-uppercase">current series</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainJumbotron",
};
</script>

<style lang="scss" scoped>
@import "../components/style.scss";

div.my-jumbo {
  position: relative;
  height: 500px;
  background-image: url("@/assets/img/jumbotron.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  div.abs-text {
    position: absolute;
    top: 100%;
    left: 10%;
    transform: translateY(-50%);
    background-color: $dc-blue;
    padding: 0.8rem 2.5rem;
  }
}
</style>
