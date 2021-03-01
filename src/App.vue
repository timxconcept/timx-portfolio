<template>
  <div id="app">
    <welcome-bg />
  </div>
</template>

<script>
import WelcomeBg from "@/components/WelcomeBg";

export default {
  components: {
    WelcomeBg,
  },
};
</script>

<style lang="scss">
@import "./global-style/colors.scss";
@import "./global-style/typography.scss";

body {
  background-color: $white;
}

h1 {
  @include heading-1;
}

p {
  @include large-text-bold;
}

#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $white;
}
</style>