<template>
  <v-app>
      <v-main>
        <home-page />
      </v-main>
  </v-app>
</template>

<script>
import HomePage from "./components/HomePage";

export default {
  name: "App",

  components: {
    HomePage,
  },
  data() {
    return {};
  },
};
</script>
<style lang="scss">
@import "./style/main.scss";
</style>
