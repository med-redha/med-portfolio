<template>
  <div class="home_page">
    <div class="hero_section" v-for="(item, index) in heroSection" :key="index">
      <v-img class="hero_img" src="../assets/portfolioHero.jpg" alt="">
        <div class="hero_txt">
          <div class="hero_header">{{ item.header }}</div>
          <div class="hero_subhead">{{ item.subhead }}</div>
          <div class="hero_info">{{ item.info }}</div>
          <div class="hero_actionGrp">
            <v-btn outlined dark large>{{ item.btnOne }}</v-btn>
            <v-btn icon dark href="https://www.linkedin.com/in/redha-boutahir-7a596223b/"
              ><v-icon class="v-icon">{{ item.btnTw }}</v-icon></v-btn
            >
            <v-btn icon dark href="https://github.com/med-redha"
              ><v-icon class="v-icon">{{ item.btnTh }}</v-icon></v-btn
            >
          </div>
        </div>
      </v-img>
    </div>
    <div class="bar-section">
      <div class="skills_grp">
        <div
          class="skill_imgHold"
          v-for="(skill, index) in skills"
          :key="index"
        >
          <img class="skill_img" :src="skill.img" alt="" />
        </div>
      </div>
    </div>
    <div class="projects_section">
      <div class="ps_title">Latest Projects</div>
      <div class="projects_holder">
        <project-case v-for="(cmp, index) in cases" :key="index" :cmp="cmp" />
      </div>
    </div>
  </div>
</template>

<script>
//logos
import jslogo from "../assets/jsLogo.png";
import tml from "../assets/htmlLogo.png";
import linuxLogo from "../assets/linuxLogo.png";
import vueLogo from "../assets/logo.svg";
import vuetifyLogo from "../assets/logo.png";
import sassLogo from "../assets/sasslogo.png";

//images
import prevOne from "../assets/projectprev.jpg";
import prevTwo from "../assets/alternativehero.jpg";
import prevThree from "../assets/herocandi.jpg";
//components
import ProjectCase from "./ProjectCase.vue";
export default {
  name: "HomePage",
  components: {
    ProjectCase,
  },
  data() {
    return {
      heroSection: [
        {
          img: "",
          header: "Mohamed Redha Boutahir",
          subhead: "Frontend Web Developer",
          info: "hello my name is Redha, i am a frontend web developer and this is my portfolio enjoy your time ",
          btnOne: "Contact Me",
          btnTw: "mdi-github",
          btnTh: "mdi-linkedin",
        },
      ],
      skills: [
        {
          img: tml,
        },
        {
          img: jslogo,
        },
        {
          img: vueLogo,
        },
        {
          img: vuetifyLogo,
        },
        {
          img: linuxLogo,
        },
        {
          img: sassLogo,
        },
      ],
      cases: [
        {
          img: prevOne,
          title: "Project Name",
          subtitle: "breif app explanation",
          btnOne: "Demo",
          btnTwo: "mdi-github",
        },
        {
          img: prevTwo,
          title: "Project Name",
          subtitle: "breif app explanation",
          btnOne: "Demo",
          btnTwo: "mdi-github ",
        },
        {
          img: prevThree,
          title: "Project Name",
          subtitle: "breif app explanation",
          btnOne: "Demo",
          btnTwo: "mdi-github",
        },
      ],
    };
  },
};
</script>
