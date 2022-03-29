<template>
  <header>
    <div>
      <img src="../assets/img/dc-logo.png" alt="dc logo" />
    </div>
    <div>
      <ul>
        <li :key="index" v-for="(link, index) in headerNav">
          <a :href="link.url">
            {{ link.text }}
          </a>
        </li>
      </ul>
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
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-transform: uppercase;
  font-weight: 600;
  font-size: 0.8rem;
  ul {
    list-style: none;
    li {
      display: inline;
      padding: 0 1.5rem;
      a {
        text-decoration: none;
        color: black;
      }
    }
  }
}
</style>
