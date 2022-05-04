<template>
  <button class="heart">
    <svg
      width="16"
      height="16"
      viewBox="0 0 16 16"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        class="st0"
        d="M7.9,3.1C6.7-2.5-2.6,1.9,1.8,7.6c4.4,5.7,6.6,7.9,6.6,7.9"
        fill="white"
      />
      <path
        class="st0"
        d="M7.9,3.1c1.2-5.6,10.8-1.2,6.5,4.5c-4.4,5.7-6.7,7.9-6.7,7.9"
        fill="white"
      />
      <path class="st0" d="M7.4,2.7l1,0l0,0.5h-1V2.7z" fill="white" />
    </svg>
  </button>
</template>
<script>
import ButtonUi from "@/components/Ui/ButtonUi.vue";
export default {
  name: "HeartComponent",
  components: {
    ButtonUi,
  },

  data() {
    return {
      color: "white",
    };
  },
};
</script>
<style lang="scss" scoped>
.heart {
  width: 44px;
  height: 44px;

  background: #333333;
  /* Brand / Black */

  border: 1px solid #333333;
  box-sizing: border-box;
}
</style>
