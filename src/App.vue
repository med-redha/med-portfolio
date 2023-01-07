<template>
  <v-app>
      <v-main>
        <home-page />
      </v-main>
       <v-footer  color="#1F1F1A"   height="800">
        <div class="footer">
          <div class="contact_box mb-2">
            <div class="contact_title"></div>
            <div class="box_row my-2">
              <div class="box_txt mb-1">name</div>
              <input class="box_input" type="text">
            </div>
            <div class="box_row my-2">
              <div class="box_txt mb-1">email</div>
              <input class="boxMail_input" type="text">
            </div>
            <div class="box_row">
              <div class="box_txt mb-1">message</div>
              <textarea  class="boxMsg_input" name="message text"  cols="30" rows="10"></textarea>
            </div>
            <div class="box_btnHolder mt-6"><v-btn color="#64644B" width="160" height="42" class="mb-2" dark>Contact Me</v-btn></div> 
          </div>
          <div class="icons_box ">
            <div class="upper_icons">
              <v-btn icon dark href="#"><v-icon class="icons">mdi-github</v-icon></v-btn>
              <v-btn icon dark href="#"><v-icon class="icons">mdi-linkedin</v-icon></v-btn>
            </div>
            <div class="lower_icons">
              <v-btn icon dark href="#"><v-icon class="icons">mdi-facebook</v-icon></v-btn>
              <v-btn icon dark href="#"><v-icon class="icons">mdi-twitter</v-icon></v-btn>
            </div>
          </div>
        </div>
      </v-footer> 
    
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
