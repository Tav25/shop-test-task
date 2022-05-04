<template>
  <div class="_container ContentComp">
    <SliderComponent style="max-width: 49.5%;"></SliderComponent>
    <ProductCardComponent style="max-width: 49.5%;"></ProductCardComponent>
    <!-- <SliderComponent></SliderComponent> -->
    <GalleryComp></GalleryComp>
  </div>
</template>

<script>
import SliderComponent from "./SliderComponent.vue";
import ProductCardComponent from "./ProductCardComponent.vue";
import GalleryComp from "./GalleryComp.vue";

export default {
  name: "ContentComp",

  components: {
    SliderComponent,
    ProductCardComponent,
    GalleryComp,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.ContentComp {
  // // width: calc(100% - 20px);
  // // height: 184px;
  // background-color: rgb(255, 255, 255);
  // // padding: 130px 5px 70px 5px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
  border: 1px solid rgba(164, 28, 146, 0.5);
}

</style>
