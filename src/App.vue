<template>
  <div class="wrapper">
    <ContentComp style=" margin-top: 64px "></ContentComp>
    <headerComp></headerComp>
    <footerComp></footerComp>
  </div>
  <!-- <ProductCardComponent></ProductCardComponent> -->
  <!-- <ButtonUi>Добавить в корзину</ButtonUi> -->
  <!-- <HeartComponent></HeartComponent> -->
  <!-- <SliderComponent /> -->
</template>

<script>
// import SliderComponent from "@/components/SliderComponent.vue";
// import ButtonUi from "@/components/Ui/ButtonUi.vue";
// import HeartComponent from "@/components/HeartComponent.vue";
// import ProductCardComponent from "@/components/ProductCardComponent.vue";
import ContentComp from "@/components/ContentComp.vue";
import footerComp from "@/components/footerComp.vue";
import headerComp from "@/components/headerComp.vue";
export default {
  name: "App",
  components: {
    // SliderComponent,
    // ButtonUi,
    // HeartComponent,
    // ProductCardComponent,
    footerComp,
    headerComp,
    ContentComp,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}

ul {
  list-style-type: none;
}

li {
  list-style-type: none;
}

#app {
  font-family: "Open Sans";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #333333;
}

.wrapper {
  min-height: 100%;
  overflow: hidden;
  border: 1px dotted rgb(0, 0, 0);
}

._container {
  max-width: 1390px;
  margin: 0 auto;
  border: 1px dotted rgb(255, 145, 0);
  padding: 0px 5px 0px 5px;
}
</style>
