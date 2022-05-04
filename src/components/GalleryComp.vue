<template>
  <div class="gallery-comp">
    <div class="gallery-comp__top">Посмотреть все стили</div>
    <div class="gallery-comp__left">
      <img src="../assets/del.jpg" alt="" />
    </div>
    <div class="gallery-comp__right">
      <div class="gallery-comp__right-small-image">
        <img src="../assets/del.jpg" alt="" />
      </div>
      <div class="gallery-comp__right-small-image">
        <img src="../assets/del.jpg" alt="" />
      </div>
      <div class="gallery-comp__right-small-image">
        <img src="../assets/del.jpg" alt="" />
      </div>
      <div class="gallery-comp__right-small-image">
        <img src="../assets/del.jpg" alt="" />
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
  // position: relative;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;

  background-color: rgb(151, 60, 255);
  // width: 100%;

  &__top {
    background-color: rgb(255, 196, 0);
    height: 28px;
    flex: 0 1 100%;

    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;

    padding: 28px 0px 28px 0px;

    font-family: "Open Sans";
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 20px;

    letter-spacing: 0.04em;
    text-decoration-line: underline;
    text-decoration-color: red;

    color: #333333;
  }

  &__left {
    background-color: rgb(60, 73, 255);
    width: 686px;
    height: 688px;
    // padding: 5px;
  }

  &__right {
    background-color: rgb(255, 60, 229);
    width: 686px;
    height: 688px;

    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;
    align-content: space-between;
  }

  &__right-small-image {
    width: calc(50% - 8px);
    height: calc(50% - 8px);
    background-color: rgb(179, 255, 2);
    // padding: 8px;
  }

  img {
    width: 100%;
    height: 100%;
  }
}
</style>
