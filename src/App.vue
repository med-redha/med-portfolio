<template>
  <v-app>
    <v-app-bar
  color="orange"
  flat
> <div class="bar">
  <div class="logo_holder">
    <img class="logo" src="./assets/portfoliologo.png" alt="">
  </div>
</div></v-app-bar>
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
