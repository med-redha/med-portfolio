<template>
  <div class="project_case " :cmp="cmp">
    <div class="img_holder">
      <img class="prj_img" :src="cmp.img" alt="" />
    </div>
    <div class="info_holder">
      <div class="info_title ">{{ cmp.title }}</div>
      <div class="info_subtitle">{{ cmp.subtitle }}</div>
      <div class="info_actionGrp ">

        <v-btn width="100"  height="58" class="btn_clr"  :href="cmp.href">{{ cmp.btnOne }}</v-btn>
        <v-btn  class="btns" icon  :href="cmp.link">
          <v-icon  class="v-icon">{{ cmp.btnTwo }}</v-icon>
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
