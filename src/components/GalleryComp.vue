<template>
  <div class="gallery-comp">
    <div class="gallery-comp__top">Посмотреть все стили</div>
    <div class="gallery-comp__left">
      <img src="../assets/g1.jpg" alt="" />
    </div>
    <div class="gallery-comp__right">
      <div class="gallery-comp__right-small-image">
        <img src="../assets/g2.jpg" alt="" />
      </div>
      <div class="gallery-comp__right-small-image">
        <img src="../assets/g3.png" alt="" />
      </div>
      <div class="gallery-comp__right-small-image">
        <img src="../assets/g4.png" alt="" />
      </div>
      <div class="gallery-comp__right-small-image">
        <img src="../assets/g5.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GalleryComp",
  props: {},

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
.gallery-comp {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;

  background-color: rgb(151, 60, 255);

  &__top {
    background-color: rgb(255, 196, 0);
    height: 28px;
    flex: 0 1 100%;

    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;

    padding: 28px 0px 56px 0px;

    letter-spacing: 0.04em;
    text-decoration-line: underline;
    text-decoration-color: red;
  }

  &__left {
    background-color: rgb(60, 73, 255);
    max-width: 49.3%;
    img {
      width: 100%;
      height: 100%;
    }
  }

  &__right {
    background-color: rgb(255, 60, 229);
    max-width: 49.3%;

    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;
    align-content: space-between;
  }

  &__right-small-image {
    width: 48.8%;
    margin-bottom: 2.4%;
    img {
      width: 100%;
      // height: 10%;
    }
  }
}
</style>
