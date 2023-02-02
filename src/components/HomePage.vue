<template>
  <div class="home_page">
    <div class="hero_section" v-for="(item, index) in heroSection" :key="index">
      <v-img class="hero_img" src="../assets/portfolioHero.jpg" alt="">
        <div class="hero_txt">
          <div class="hero_info">{{ item.info }}</div>
          <div class="hero_subhead">{{ item.subhead }}</div>
          <div class="hero_header">{{ item.header }}</div>

          <div class="hero_actionGrp">
            <v-btn icon dark href="https://github.com/med-redha"
              ><v-icon class="v-icon">{{ item.btnTw }}</v-icon></v-btn
            >
            <v-btn
              icon
              dark
              href="https://www.linkedin.com/in/redha-boutahir-7a596223b/"
              ><v-icon class="v-icon">{{ item.btnTh }}</v-icon></v-btn
            >
          </div>
        </div>
      </v-img>
    </div>
    <div class="About_me" v-for="(elem, index) in aboutMe" :key="index">
      <div class="me_title">{{ elem.title }}</div>
      <div class="me_content">
        <div class="me_imageHolder">
          <img class="me_img" :src="elem.img" alt="redha boutahir" />
        </div>
        <div class="me_discription">{{ elem.description }}</div>
      </div>
    </div>
    <div class="skills_container">
      <my-skills />
    </div>

    <div class="my_projects">
      <project-case v-for="(cmp, index) in cases" :key="index" :cmp="cmp" />
    </div>
  </div>
</template>

<script>
//logos
//images
import projectOne from "../assets/projectOne.png";
import projectTwo from "../assets/snapchallenge.png";
import projectThree from "../assets/femlandingpage.png";
import logo from "../assets/portfoliologo.png";

//import prevThree from "../assets/herocandi.jpg";
//components
import ProjectCase from "./ProjectCase.vue";
import mySkills from "./MySkills.vue";
export default {
  name: "HomePage",
  components: {
    ProjectCase,
    mySkills,
  },
  data() {
    return {
      heroSection: [
        {
          img: "",
          header: "INNOVATe,ASPIRE, REALIZE",
          subhead: "Frontend Web Developer",
          info: "Hello My Name Is Redha, I Am a Frontend Web Developer",
          btnTw: "mdi-github",
          btnTh: "mdi-linkedin",
        },
      ],
      aboutMe: [
        {
          img: logo,
          title: "About Me",
          description:
            "Hi! I am Redha Boutahir, a web designer/developer focused on crafting great web experiences. Designing and Coding have been my passion since the days I started working with computers but I found myself into web design/development since 2022. I enjoy creating beautifully designed, intuitive and functional websites.",
        },
      ],

      cases: [
        {
          img: projectOne,
          title: "fem-product-card",
          subtitle: "Mobile first design,product card made with purely html and css.  This was a challenge of frontend mentor.  ",
          btnOne: "Demo",
          href: 'https://fem-productcardbyredha.netlify.app/',
          btnTwo: "mdi-github",
          link: 'https://github.com/med-redha/fem-productCard',
        },
        {
          img: projectTwo,
          title: "Intro-section",
          subtitle: "frontend mentor Challenge, made with vue.js,vuetify, mobile first design",
          btnOne: "Demo",
          href:'https://fem-snapchallenge-by-redha.netlify.app/',
          btnTwo: "mdi-github ",
          link:'https://github.com/med-redha/fem-snapchallenge',
        },
        {
          img: projectThree,
          title: "Home-page",
          subtitle: "Landing page,mobile first design,with vue.js,vuetify,scss",
          btnOne: "Demo",
          href: 'https://femlandingpageredhaboutahir.netlify.app/',
          btnTwo: "mdi-github",
          link: 'https://github.com/med-redha/home-page',
        },
      ],
    };
  },
};
</script>
