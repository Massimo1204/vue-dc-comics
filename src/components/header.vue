<template>
  <div>
    <header>
      <div>
        <img src="../assets/img/dc-logo.png" alt="dc logo" />
      </div>
      <div>
        <ul></ul>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "mainHeader",
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
<style scoped lang="scss"></style>
