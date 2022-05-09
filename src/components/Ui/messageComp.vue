<template>
  <div @click="top" class="message" :style="{ top: topData + 'px' }">
    <span><slot></slot>{{ topData }}</span>
  </div>
</template>
<script>
export default {
  name: "messageComp",
  data() {
    return {
      topData: 0,
      rez: ``,
    };
  },
  methods: {
    top: function () {
      this.topData = window.pageYOffset + 100;
    },
  },

  beforeMount() {
    this.topData = window.pageYOffset + 100;
  },
};
</script>
<style lang="scss" scoped>
.message {
  position: absolute;
  // top: 50%;
  left: 25%;
  z-index: 100;

  width: 50%;

  display: flex;
  justify-content: center;
  align-items: center;

  background: #ffffff;
  /* Brand / Black */

  border: 2px solid #ffa600;

  font-family: "Open Sans";
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 250%;
  /* identical to box height, or 143% */

  letter-spacing: 0.04em;

  /* Brand / White */

  color: #001a3b;
}
</style>
