<template>
  <div class="blockRegMail">
    <div class="blockRegMail__title">Узнайте первыми о новинках и акциях</div>

    <div class="blockRegMail__input-mail">
      <input type="text" placeholder="Адрес электронной почты" />
      <div>
        <svg
          width="10"
          height="10"
          viewBox="0 0 10 10"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M0.700012 9.06641L9.05007 0.88337" stroke="#C4C4C4" />
          <path d="M9.25165 9.06641L0.901606 0.883353" stroke="#C4C4C4" />
        </svg>
      </div>
    </div>
    <div class="blockRegMail__btn">
      <ButtonBorderUi>Подписаться</ButtonBorderUi>
    </div>
  </div>

<messageComp>Alert</messageComp>
</template>

<script>
import ButtonBorderUi from "./Ui/ButtonBorderUi.vue";
import messageComp from "./Ui/messageComp.vue";
export default {
  name: "blockRegMail",
  components: {
    ButtonBorderUi,
    messageComp
  },
  data() {
    return {
      email: "",
      isEmailTrue: false,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.blockRegMail {
  width: 452px;
  margin: 0px 8px 0px 8px;
  // background-color: rgb(236, 227, 227);

  &__title {
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;

    letter-spacing: 0.04em;
    text-transform: uppercase;

    color: #333333;

    flex: none;
    order: 0;
    flex-grow: 0;
    // margin: 0px 10px;
    padding-top: 12px;
    padding-bottom: 12px;
  }

  &__input-mail {
    height: 44px;

    border-bottom: 2px solid #c4c4c4;

    color: #333333;

    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 0px 8px 0px 16px;
    margin: 22px 0px 24px 0px;

    input {
      width: calc(100% - 16px);
      border: none;
      border-width: 0;
      border: 0;
      background-color: rgba(255, 255, 255, 0);
      outline: none;

      font-family: "Open Sans";
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 20px;
      /* identical to box height, or 143% */

      letter-spacing: 0.04em;
    }
  }

  &__btn {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    margin-top: 32px;
  }
}
</style>
