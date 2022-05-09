<template>
  <div class="blockBuer">
    <div class="blockBuer__title">{{ title }}</div>
    <ul>
      <li class="blockBuer__item" v-for="item in menu">
        <a :href="item.link">{{ item.text }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "blockBuer",
  props: {
    title: String,
    menu: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.blockBuer {
  min-width: 200px;
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
    line-height: 160%;
    letter-spacing: 0.04em;

    flex: none;
    order: 0;
    flex-grow: 0;
    padding-top: 4px;
  }

  &__item:nth-last-child(1) {
    padding-bottom: 20px;
  }

  li {
  }
}
</style>
