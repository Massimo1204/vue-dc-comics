<template>
  <div class="mainNav-container">
    <div v-for="(link, index) in mainNav" :key="index">
      <img :src="link.imgSrc" :alt="link.title" :href="link.url" />
    </div>
  </div>
</template>

<script>
export default {
  name: "mainNavigation",
  data: function () {
    return {
      mainNav: [
        {
          imgSrc: "../assets/img/buy-comics-digital-comics.png",
          url: "#",
          title: "Digital comics",
        },
        {
          imgSrc: "../assets/img/buy-comics-merchandise.png",
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

<style lang="scss" scoped></style>
