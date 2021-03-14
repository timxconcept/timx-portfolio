<template>
  <div id="app">
    <main-screen />
  </div>
</template>

<script>
import MainScreen from "@/components/MainScreen";

export default {
  name: "App",
  components: {
    MainScreen,
  },
  metaInfo: {
    // if no subcomponents specify a metaInfo.title, this title will be used
    title: "Default Title",
    // all titles will be injected into this template
    titleTemplate: "%s | My Awesome Webapp",
  },
};
</script>

<style lang="scss">
@import "./global-style/colors.scss";
@import "./global-style/typography.scss";

body {
  background-color: $white;
  padding: 0;
  margin: 0;
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

#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $white;
  max-height: 100vh;
}
</style> 