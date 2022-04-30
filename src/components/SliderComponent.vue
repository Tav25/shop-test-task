<template>
  <div class="slider">
    <img :src="slider.path + slider.images[slider.currentImage].scr" alt="" />
    <div class="slider__prew-images">
      <!-- <li v-for="n in slider.images">{{ n }}</li> -->
      <div v-for="(item, index) in slider.images" :key="item">
        <img
          v-on:click="test2(index)"
          :src="slider.path + item.scr"
          :alt="item.alt"
          :data-set="index"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SliderComponent",
  props: {},

  data: function () {
    return {
      slider: {
        path: "/images/slider/",
        currentImage: 0,
        images: [
          { id: "bc011", scr: "img1.jpg", alt: "images 01" },
          { id: "bc012", scr: "img2.jpg", alt: "images 02" },
        ],
      },
    };
  },
  methods: {
    test2: function (index) {
      this.slider.currentImage = index;
      console.log(index);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.slider {
  position: relative;
  width: 686px;
  height: 923px;
  // width: 200px;
  // height: 300px;
  background-color: rgb(89, 250, 129);

  img {
    width: 100%;
    height: 100%;
  }

  &__prew-images {
    position: absolute;
    top: 3px;
    left: 3px;
    width: 20%;
    height: 50%;
    background-color: rgb(255, 196, 1);

    img {
      width: 100px;
      height: 100px;
    }
  }
}
</style>
