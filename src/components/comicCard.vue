<template>
  <div>
    <div class="card" v-for="(element, index) in cards" :key="index">
      <a href="#">
        <div class="img-wrapper">
          <img :src="element.thumb" alt="element.type" />
        </div>
        <h3 class="text-uppercase">{{ element.series }}</h3>
      </a>
    </div>
    <div class="btn-wrapper">
      <button class="text-uppercase">load more</button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["cards"],
};
</script>

<style lang="scss" scoped>
@import "../components/style.scss";

div {
  @include flexed(row, center, center);
  flex-wrap: wrap;
  padding: 1.3rem 0 0.8rem 0;
  div.card {
    @include flexed(column, center, start);
    width: calc((100% / 6) - 2.3rem);
    height: 350px;
    margin: 0 1.15rem;
    a {
      text-decoration: none;
      width: 100%;
      height: 100%;
      div.img-wrapper {
        height: 250px;
        width: 100%;
        overflow: hidden;
        img {
          width: 100%;
        }
      }
      h3 {
        padding-top: 1.5rem;
        color: white;
      }
    }
  }
  div.btn-wrapper {
    margin-top: 2rem;
    button {
      padding: 0.8rem 3.5rem;
      background-color: $dc-blue;
      font-weight: 600;
      color: white;
    }
  }
}
</style>
