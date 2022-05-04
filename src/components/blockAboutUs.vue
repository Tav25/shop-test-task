<template>
  <div class="blockAboutUs">
    <div class="title">покупателям</div>
    <li><a href="https://">Каталог</a></li>
    <li><a href="https://">Акции</a></li>
    <li><a href="https://">Бренды</a></li>
  </div>
</template>

<script>
export default {
  name: 'blockAboutUs',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.blockAboutUs {
  min-width: 335px;
  margin: 0px 8px 0px 8px;
  background-color: rgb(202, 29, 255);
}
</style>
