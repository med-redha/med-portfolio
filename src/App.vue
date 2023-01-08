<template>
  <v-app>
      <v-main>
        <home-page />
      </v-main>
       <v-footer  color="#1F1F1A"   height="800">
        <div class="footer">
          <div class="contact_box ">
            <div class="contact_title"></div>
            <div class="box_row ">
              <div class="box_txt ">name</div>
              <input class="box_input" type="text">
            </div>
            <div class="box_row ">
              <div class="box_txt ">email</div>
              <input class="boxMail_input" type="text">
            </div>
            <div class="box_row">
              <div class="box_txt ">message</div>
              <textarea  class="boxMsg_input" name="message text"  cols="30" rows="10"></textarea>
            </div>
            <div class="box_btnHolder "><v-btn color="#64644B" width="160" height="42" class="mb-2" dark>Contact Me</v-btn></div> 
          </div>
          <div class="icons_box ">
            <div class="upper_icons">
              <v-btn icon dark href="https://github.com/med-redha"><v-icon class="icons">mdi-github</v-icon></v-btn>
              <v-btn icon dark href="https://www.linkedin.com/in/redha-boutahir-7a596223b/"><v-icon class="icons">mdi-linkedin</v-icon></v-btn>
            </div>
            <div class="lower_icons">
              <v-btn icon dark href="https://www.facebook.com/profile.php?id=100078919627069"><v-icon class="icons">mdi-facebook</v-icon></v-btn>
              <v-btn icon dark href="https://twitter.com/RedhaBoutahir"><v-icon class="icons">mdi-twitter</v-icon></v-btn>
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
