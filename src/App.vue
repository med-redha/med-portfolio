<template>
  <v-app>
    <v-container>
      <v-main>
        <home-page />
      </v-main>
      <v-footer color="#1F1F1A" max-width="1280" height="800">
        <div class="footer">
          <div class="contact_box">
            <div class="contact_title"></div>
            <div class="box_row">
              <div class="box_txt">name</div>
              <input class="box_input" type="text">
            </div>
            <div class="box_row">
              <div class="box_txt">email</div>
              <input class="boxMail_input" type="text">
            </div>
            <div class="box_row">
              <div class="box_txt">message</div>
              <input class="boxMsg_input" type="text">
            </div>
            <div class="box_btnHolder"><v-btn> <span class="btntxt">Contact Me</span></v-btn></div> 
          </div>
          <div class="icons_box">
            <div class="upper_icons">
              <v-btn icon dark><v-icon large>mdi-github</v-icon></v-btn>
              <v-btn icon dark><v-icon large>mdi-linkedin</v-icon></v-btn>
            </div>
            <div class="lower_icons">
              <v-btn icon dark><v-icon large>mdi-facebook</v-icon></v-btn>
              <v-btn icon dark><v-icon large>mdi-twitter</v-icon></v-btn>
            </div>
          </div>
        </div>
      </v-footer>
    </v-container>
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
