<template>
  <footer>
    <div class="w-80">
      <div class="footer-list">
        <div>
          <h3>Dc comics</h3>
          <ul>
            <li v-for="(element, index) in comics" :key="index">
              {{ element }}
            </li>
          </ul>
          <h3>shop</h3>
          <ul>
            <li v-for="(element, index) in shop" :key="index">{{ element }}</li>
          </ul>
        </div>
        <div>
          <h3>dc</h3>
          <ul>
            <li v-for="(element, index) in dc" :key="index">{{ element }}</li>
          </ul>
        </div>
        <div>
          <h3>sites</h3>
          <ul>
            <li v-for="(element, index) in sites" :key="index">
              {{ element }}
            </li>
          </ul>
        </div>
      </div>
      <div class="dc-logo"></div>
    </div>
    <FooterBottom />
  </footer>
</template>

<script>
import FooterBottom from "./FooterBottom.vue";
export default {
  name: "indexFooter",
  components: {
    FooterBottom,
  },
  data: function () {
    return {
      comics: [
        "Characters",
        "Comics",
        "Movies",
        "TV",
        "Games",
        "Videos",
        "News",
      ],
      shop: ["Shop DC", "Shop DC Collectibles"],
      dc: [
        "Terms Of Use",
        "Privacy policy(New)",
        "Ad Choices",
        "Advertising",
        "Jobs",
        "Subscriptions",
        "Talent Workshops",
        "CPSC Certificates",
        "Ratings",
        "Shop Help",
        "Contact Us",
      ],
      sites: ["DC", "MAD Magazine", " DC Kids", "DC Universe", "DC Power Visa"],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../components/style.scss";

footer {
  background-image: url("../assets/img/footer-bg.jpg");
  div {
    @include flexed(row, space-between, start);
    div.footer-list {
      margin-top: 1.5rem;
      div {
        @include flexed(column, start, start);
        h3 {
          text-transform: uppercase;
          padding: 1rem 0;
        }
        ul {
          list-style: none;
          margin-right: 2rem;
          li {
            font-size: 0.78rem;
            line-height: 1.3rem;
            color: rgb(148, 147, 147);
          }
        }
      }
    }
    div.dc-logo {
      height: 370px;
      width: 600px;
      background-image: url("../assets/img/dc-logo-bg.png");
      background-position: center;
      background-repeat: no-repeat;
    }
  }
}
</style>
