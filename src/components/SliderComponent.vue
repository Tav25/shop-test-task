<template>
  <div class="slider">
      <img :src="slider.path + slider.images[slider.currentImage].scr" alt="" />
    <div class="slider__prew-images">
      <!-- <li v-for="n in slider.images">{{ n }}</li> -->
      <div v-for="(item, index) in slider.images" :key="item">
        <img class="ibg"
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
          { id: "bc011", scr: "img1.jpg", alt: "images 01" },
          { id: "bc011", scr: "img1.jpg", alt: "images 01" },
          { id: "bc011", scr: "img1.jpg", alt: "images 01" },
          { id: "bc012", scr: "img2.jpg", alt: "images 02" },
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
  // width: 686px;
  max-width: 100%;
  // width: 500px;
  // border: 1px dotted rgb(234, 0, 255);

    // object-fit: fill;
  img {
    // border: 1px dotted rgb(0, 255, 234);
    min-width: 100%;
    height: 100%;
  }

  &__prew-images {
    position: absolute;
    top: 2.7%;
    left: 3.5%;
    max-width: 10%;
    // height: 50%;
    // //   // background-color: rgb(255, 196, 1);
    border: 1px dotted rgba(164, 28, 146, 0.5);

    img {
      width: 100%;
      // height: 91px;
      margin-bottom: 10%;
    }
  }
}

//

//
</style>
