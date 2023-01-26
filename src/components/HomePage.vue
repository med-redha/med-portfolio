<template>
  <div class="home_page">
    <div class="hero_section" v-for="(item, index) in heroSection" :key="index">
      <v-img class="hero_img" src="../assets/portfolioHero.jpg" alt="">
        <div class="hero_txt">
          <div class="hero_header">{{ item.header }}</div>
          <div class="hero_subhead">{{ item.subhead }}</div>
          <div class="hero_info">{{ item.info }}</div>
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
    <div class="About_me" v-for="(item, index) in aboutMe" :key="index">
      <div class="me_title">{{ item.title }}</div>
      <div class="me_content">
        <div class="me_imageHolder">
          <img class="me_img" :src="item.img" alt="redha boutahir" />
        </div>
        <div class="me_discription">{{ item.description }}</div>
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
import tml from "../assets/htmlLogo.png";

//images
import prevOne from "../assets/projectprev.jpg";
import prevTwo from "../assets/alternativehero.jpg";
import prevThree from "../assets/herocandi.jpg";
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
          header: "Mohamed Redha Boutahir",
          subhead: "Frontend Web Developer",
          info: "hello my name is Redha, i am a frontend web developer and this is my portfolio enjoy your time ",
          btnTw: "mdi-github",
          btnTh: "mdi-linkedin",
        },
      ],
      aboutMe: [
        {
          img: tml,
          title: "About Me",
          description:
            "Hi! I am Redha Boutahir, a web designer/developer focused on crafting great web experiences. Designing and Coding have been my passion since the days I started working with computers but I found myself into web design/development since 2022. I enjoy creating beautifully designed, intuitive and functional websites.",
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
