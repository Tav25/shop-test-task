<template>
  <button class="btn"><slot></slot></button>
</template>
<script>
export default {
  name: "ButtonUi",
};
</script>
<style lang="scss" scoped>
.btn {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 8px 28px;

  /* Brand / Black */

  background: #333333;
  /* Brand / Black */

  border: 1px solid #333333;
  box-sizing: border-box;

  /* Inside auto layout */

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;

  font-family: "Open Sans";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  letter-spacing: 0.04em;

  /* Brand / White */

  color: #ffffff;
}
</style>
