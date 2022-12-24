<template>
  <div class="project_case " :cmp="cmp">
    <div class="img_holder">
      <img class="prj_img" :src="cmp.img" alt="" />
    </div>
    <div class="info_holder">
      <div class="info_title my-2">{{ cmp.title }}</div>
      <div class="info_subtitle">{{ cmp.subtitle }}</div>
      <div class="info_actionGrp my-8">

        <v-btn   width="90" height="45"   class="btn_clr" >{{ cmp.btnOne }}</v-btn>
        <v-btn icon  dark class="ml-4">
          <v-icon class="v-icon">{{ cmp.btnTwo }}</v-icon>
        </v-btn>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cmp: Object,
  },
};
</script>
