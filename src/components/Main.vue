<template>
  <nav>
    <div v-for="(element, index) in navList" :key="index">
      <img
        :src="require(`../assets/img/${element.imgSrc}`)"
        :alt="element.title"
      />
      <h5 class="text-uppercase">{{ element.title }}</h5>
    </div>
  </nav>
</template>

<script>
export default {
  name: "mainNavigation",
  data: function () {
    return {
      navList: [
        {
          imgSrc: "buy-comics-digital-comics.png",
          url: "#",
          title: "Digital comics",
        },
        {
          imgSrc: "buy-comics-merchandise.png",
          url: "#",
          title: "DC merchandise",
        },
        {
          imgSrc: "buy-comics-subscriptions.png",
          url: "#",
          title: "subscription",
        },
        {
          imgSrc: "buy-comics-shop-locator.png",
          url: "#",
          title: "comic shop locator",
        },
        {
          imgSrc: "buy-dc-power-visa.svg",
          url: "#",
          title: "DC power visa",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../components/style.scss";

nav {
  background-color: $dc-blue;
  height: 100px;
  @include flexed(row, space-evenly, center);
  div {
    @include flexed(row, start, center);
    img {
      height: 50px;
    }
    h5 {
      padding-left: 0.5rem;
    }
  }
}
</style>
