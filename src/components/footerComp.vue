<template>
  <div class="_container footerComp">
    <blockBuer class="w24" :title="menu1.title" :menu="menu1.data"></blockBuer>
    <blockBuer class="w24" :title="menu2.title" :menu="menu2.data"></blockBuer>
    <blockRegMail></blockRegMail>
  </div>
</template>

<script>
import blockBuer from "./blockBuer.vue";
import blockRegMail from "./blockRegMail.vue";

export default {
  name: "footerComp",

  components: {
    blockBuer,
    blockRegMail,
  },

  data() {
    return {
      menu1: {
        title: "покупателям",
        data: [
          { text: "Каталог", link: "/" },
          { text: "Акции", link: "/" },
          { text: "Бренды", link: "/" },
        ],
      },
      menu2: {
        title: "о нас",
        data: [
          { text: "О компании", link: "/" },
          { text: "Новости", link: "/" },
          { text: "Команда", link: "/" },
          // { text: "dfdfd4", link: "/" },
        ],
      },
    };
  },
};
</script>

<style scoped lang="scss">
.footerComp {
  background-color: rgb(255, 255, 255);
  padding-top: 115px;
  padding-bottom: 70px;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-wrap: wrap;
  // background-color: rgb(245, 245, 245);
  // border: 1px solid rgba(28, 110, 164, 0.5);
}

.w24 {
  width: 24%;
}
</style>
