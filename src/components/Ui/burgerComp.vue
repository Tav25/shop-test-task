<template>
  <div>
    <div v-if="show"  class="burger-menu">
      <div v-on:click="test" class="burger-menu__hide">
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <line
            x1="5.01046"
            y1="18.2822"
            x2="18.6464"
            y2="4.6462"
            stroke="#333333"
          />
          <line
            y1="-0.5"
            x2="19.2842"
            y2="-0.5"
            transform="matrix(-0.707107 -0.707107 -0.707107 0.707107 19 18.6357)"
            stroke="#333333"
          />
        </svg>
      </div>
      <div class="burger-menu__nav">
        <ul>
          <li>постельное белье</li>
          <li>одежда для дома</li>
          <li>Одежда для улицы</li>
          <li>ВЫход</li>
        </ul>
      </div>
    </div>
    <div class="burger" v-on:click="test">
      <div class="burger__line"></div>
      <div class="burger__line"></div>
      <div class="burger__line"></div>
    </div>
    <!-- {{ cd }} -->
    <!-- <h1 v-if="show">Vue восхитителен!</h1> -->
  </div>
</template>
<script>
export default {
  name: "burgerComp",

  data() {
    return {
      show: false,
      cd: 0,
    };
  },

  methods: {
    test: function () {
      console.log("<><><>");
      this.show = !this.show;
      this.cd += 1;
    },
  },
};
</script>
<style lang="scss" scoped>
.burger {
  width: 18px;
  height: 13px;
  // background-color: rgb(238, 255, 0);

  display: flex;
  flex-direction: column;
  justify-content: space-between;
  &__line {
    width: 100%;
    height: 1px;
    background-color: #333;
  }
}

.burger-menu {
  position: absolute;
  top: 0;
  left: 0;

  width: 100%;
  min-height: 200px;
  background-color: #fff;

  &__nav {
    padding-top: 20px;
    padding-left: 80px;

    li{
      line-height: 200%;
    }
  }

  &__hide {
    // position: relative;
    // background-color: rgb(208, 255, 0);
    height: 24px;
    margin-top: 20px;
    // width: px;
    // top: 18px;
    // left: calc(100% - 18px - 20px);
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
}
</style>
