<template>
  <!-- <div class="productQuantity">4545454</div> -->
  <div class="productQuantity">
    <div v-on:click="counterUp" class="productQuantity__up active">+</div>
    <div class="productQuantity__quantity">{{ counter }}</div>
    <div v-on:click="counterDown" class="productQuantity__down active">–</div>
  </div>
</template>

<script>
export default {
  name: "productQuantity",
  data() {
    return {
      counter: 1,
      max: 99,
      min: 1,
    };
  },

  methods: {
    counterUp: function () {
      this.counter < this.max ? (this.counter += 1) : this.counter;
    },
    counterDown: function () {
      this.counter > this.min ? (this.counter -= 1) : this.min;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.productQuantity {
  width: 145px;
  height: 44px;

  display: flex;
  justify-content: space-between;
   background: #f2f2f2;


   

  &__down {
    flex: 0 1 33.3%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  &__quantity {
    flex: 0 1 33.3%;
    display: flex;
    justify-content: center;
    align-items: center;
    // background-color: rgb(138, 68, 68);
  }

  &__up {
    flex: 0 1 33.3%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .active:hover {
    cursor: pointer;
    background: #e4e4e4;
    transition: 0.25s;
  }
}
</style>
