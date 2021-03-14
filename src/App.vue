<template>
  <div class="app" :class="mode == 'dark' ? 'dark' : 'light'">
    <main-screen :mode="mode" @toggle="toggle" />
  </div>
</template>

<script>
import MainScreen from "./components/MainScreen.vue";

export default {
  name: "App",
  data() {
    return {
      mode: "light",
    };
  },
  components: {
    MainScreen,
  },

  methods: {
    toggle() {
      if (this.mode == "dark") {
        this.mode = "light";
      } else {
        this.mode = "dark";
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./global-style/colors.scss";
@import "./global-style/typography.scss";

body {
  padding: 0;
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  overflow: hidden;
}
* {
  box-sizing: border-box;
}

h1 {
  @include heading-1;
}

p {
  @include large-text-bold;
}

.add {
  background-color: $white;
  color: $black;
  transition: background-color 0.3s;
}

.dark {
  background-color: $black;
  color: $white;
}
</style> 