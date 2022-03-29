<template>
  <div>
    <h1>ciao</h1>
    <div>
      <ul>
        <li v-for="(link, index) in mainNav" :key="index">
          <a href="">
            <img :src="require(link.imgSrc)" alt="link-title" />
            <h4>{{ link.title }}</h4>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainNav",
  data: function () {
    return {
      mainNav: [
        {
          imgSrc: "../assets/img/buy-comics-digital-comics.png",
          url: "#",
          title: "Digital comics",
        },
        {
          imgSrc: "..assets/img/buy-comics-merchandise.png",
          url: "#",
          title: "DC merchandise",
        },
        {
          imgSrc: "../assets/img/buy-comics-subscriptions.png",
          url: "#",
          title: "subscription",
        },
        {
          imgSrc: "../assets/img/buy-comics-shop-locator.png",
          url: "#",
          title: "comic shop locator",
        },
        {
          imgSrc: "../assets/img/buy-dc-power-visa.svg",
          url: "#",
          title: "DC power visa",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
main {
  color: black;
  background-color: red;
}
</style>
