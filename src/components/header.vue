<template>
  <header class="text-uppercase">
    <div class="w-80">
      <div>
        <img src="../assets/img/dc-logo.png" alt="dc logo" />
      </div>
      <div>
        <ul>
          <li :key="index" v-for="(link, index) in headerNav">
            <a
              :class="link.state ? 'active' : ''"
              :href="link.url"
              @click="changeState(index)"
            >
              {{ link.text }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "indexHeader",
  data: function () {
    return {
      headerNav: [
        {
          text: "characters",
          url: "#",
          state: false,
        },
        {
          text: "comics",
          url: "#",
          state: true,
        },
        {
          text: "movies",
          url: "#",
          state: false,
        },
        {
          text: "tv",
          url: "#",
          state: false,
        },
        {
          text: "games",
          url: "#",
          state: false,
        },
        {
          text: "collectibles",
          url: "#",
          state: false,
        },
        {
          text: "videos",
          url: "#",
          state: false,
        },
        {
          text: "fans",
          url: "#",
          state: false,
        },
        {
          text: "news",
          url: "#",
          state: false,
        },
        {
          text: "shop",
          url: "#",
          state: false,
        },
      ],
    };
  },
  methods: {
    changeState(index) {
      this.headerNav.forEach((element) => {
        element.state = false;
      });
      this.headerNav[index].state = true;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../components/style.scss";

header {
  padding: 0.7rem;
  div {
    @include flexed(row, space-between, center);
    font-weight: 600;
    font-size: 0.9rem;
    div {
      img {
        height: 80px;
      }
    }
    ul {
      list-style: none;
      li {
        display: inline;
        padding: 0 0.8rem;
        a {
          text-decoration: none;
          color: black;
          padding: 38px 0;
        }
        a.active {
          border-bottom: 5px solid $dc-blue;
          color: $dc-blue;
        }
      }
    }
  }
}
</style>
