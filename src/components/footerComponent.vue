<template>
  <footer class="_container footerComp">
    <blockBuer msg="покупателям" />
    <blockBuer msg="о нас" />
    <blockRegMail />
  </footer>
</template>

<script>
import blockBuer from "./blockBuer.vue";
import blockAboutUs from "./blockAboutUs.vue";
import blockRegMail from "./blockRegMail.vue";

export default {
  name: "footerComp",

  components: {
    blockBuer,
    blockAboutUs,
    blockRegMail,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.footerComp {
  // width: 100;
  // height: 184px;
  padding-top: 130px;
  padding-bottom: 70px;

  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-wrap: wrap;
  // background-color: rgb(255, 255, 255);
  background-color: rgb(245, 245, 245);
  // border: 1px solid rgba(28, 110, 164, 0.5);
}
</style>
