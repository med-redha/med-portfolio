<template>
  <div class="home_page">
    <div class="hero_section" v-for="(item, index) in heroSection" :key="index">
      <v-img class="hero_img" src="../assets/portfolioHero.jpg" alt=""> 
        <div class="hero_txt ml-8">
        <div class="hero_header">{{ item.header }}</div>
        <div class="hero_subhead">{{ item.subhead }}</div>
        <div class="hero_info">{{ item.info }}</div>
        <div class="hero_actionGrp">
          <v-btn depressed dark>{{ item.btnOne }}</v-btn>
          <v-btn icon dark><v-icon large>{{ item.btnTw }}</v-icon></v-btn>
          <v-btn icon dark><v-icon large>{{ item.btnTh }}</v-icon></v-btn>
        </div>
      </div>
      </v-img>
      
    </div>
    <div class="bar-section ">
      <div class="skills_grp"></div>
    </div>
    <div class="projects_section mt-16">
      <div class="ps_title mt-16">Latest Projects</div>
      <div class="ps_title">Latest Projects</div>
      <div class="ps_title">Latest Projects</div>
      <div class="ps_title">Latest Projects</div>
      <div class="ps_title">Latest Projects</div>
      <div class="ps_title">Latest Projects</div>
      <div class="ps_title">Latest Projects</div>
      <div class="ps_title">Latest Projects</div>
      <div class="ps_title">Latest Projects</div>
      <div class="projects_holder">
        <project-case v-for="(cmp,index) in cases " :key="index" :cmp="cmp"/>
      </div>
    </div>
  </div>
</template>

<script>
import prevOne from '../assets/projectprev.jpg';
import prevTwo from '../assets/alternativehero.jpg';
import prevThree from '../assets/herocandi.jpg';
import ProjectCase from './ProjectCase.vue';
export default {
  name: "HomePage",
components:{
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
      cases:[
        {
          img:prevOne,
          title:'Project Name',
          subtitle:'breif app explanation',
          btnOne:'Demo',
          btnTwo:'mdi-github',
          btnTwtxt:'Code',
        },
        {
          img:prevTwo,
          title:'Project Name',
          subtitle:'breif app explanation',
          btnOne:'Demo',
          btnTwo:'mdi-github',
          btnTwtxt:'Code',
        },
        {
          img:prevThree,
          title:'Project Name',
          subtitle:'breif app explanation',
          btnOne:'Demo',
          btnTwo:'mdi-github',
          btnTwtxt:'Code',
        },
      ],
    };
  },
};
</script>
