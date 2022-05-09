<template>
  <div class="wrapper">
    <ContentComp style="margin-top: 64px"></ContentComp>
    <headerComp></headerComp>
    <footerComp></footerComp>
  </div>
</template>

<script>
import ContentComp from "@/components/ContentComp.vue";
import footerComp from "@/components/footerComp.vue";
import headerComp from "@/components/headerComp.vue";
export default {
  name: "App",
  components: {
    footerComp,
    headerComp,
    ContentComp,
  },
};
</script>

<style lang="scss">
@import url(https://fonts.googleapis.com/css?family=Open+Sans:300,regular,500,600,700,800,300italic,italic,500italic,600italic,700italic,800italic);

#app {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #333333;
  min-height: 100%;
}

a {
  color: #333333;
}

.wrapper {
  overflow: hidden;
  border: 1px dotted rgb(0, 0, 0);
}

._container {
  max-width: 1400px;
  margin: 0 auto;
  border: 1px dotted rgb(255, 145, 0);
  padding: 0px 5px 0px 5px;
  // margin: 0px 5px;
}

.ibg {
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  position: relative;
}

.ibg img {
  width: 0;
  height: 0;
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0;
  visibility: hidden;
}
</style>
