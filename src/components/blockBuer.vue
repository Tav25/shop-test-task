<template>
  <div class="blockBuer">
    <div class="blockBuer__title">{{ msg }}</div>

    <li class="blockBuer__item"><a href="https://">Каталог</a></li>
    <li class="blockBuer__item"><a href="https://">Акции</a></li>
    <li class="blockBuer__item">
      <a href="https://">Бренды</a>
    </li>
  </div>
</template>

<script>
export default {
  name: "blockBuer",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.blockBuer {
  min-width: 335px;
  margin: 0px 8px 0px 8px;
  // background-color: rgb(255, 165, 29);

  &__title {
    font-size: 16px;
    line-height: 150%;
    letter-spacing: 0.04em;
    text-transform: uppercase;

    flex: none;
    order: 0;
    flex-grow: 0;
    padding-top: 12px;
    padding-bottom: 12px;
  }

  &__item {
    font-size: 14px;
    line-height: 142%;
    letter-spacing: 0.04em;

    flex: none;
    order: 0;
    flex-grow: 0;
    padding-top: 4px;
  }

  &__item:nth-last-child(1) {
    padding-bottom: 20px;
  }
}
</style>
