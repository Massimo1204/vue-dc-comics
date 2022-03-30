<template>
  <div>
    <div class="w-80">
      <div class="footer-btn-wrapper">
        <button class="text-uppercase">sign-up now!</button>
      </div>
      <div class="footer-logos">
        <h2 class="text-uppercase">Follow us</h2>
        <ul>
          <li v-for="(element, index) in logos" :key="index">
            <a :href="element.url">
              <img
                :src="require(`../assets/img/${element.imgSrc}`)"
                :alt="element.title"
              />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterBottom",
  data: function () {
    return {
      logos: [
        {
          imgSrc: "footer-facebook.png",
          title: "facebook",
          url: "#",
        },
        {
          imgSrc: "footer-twitter.png",
          title: "twitter",
          url: "#",
        },
        {
          imgSrc: "footer-youtube.png",
          title: "youtube",
          url: "#",
        },
        {
          imgSrc: "footer-pinterest.png",
          title: "pinterest",
          url: "#",
        },
        {
          imgSrc: "footer-periscope.png",
          title: "periscope",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../components/style.scss";

div {
  background-color: $footer-grey;
  div {
    @include flexed(row, space-between, center);
    padding: 0.5rem;
    div.footer-btn-wrapper {
      button {
        background-color: $footer-grey;
        border: 2px solid $dc-blue;
        padding: 0.5rem;
        color: white;
        font-weight: 600;
      }
    }
    div.footer-logos {
      color: $dc-blue;
      ul {
        list-style: none;
        li {
          display: inline;
          padding-left: 1rem;
        }
      }
    }
  }
}
</style>
