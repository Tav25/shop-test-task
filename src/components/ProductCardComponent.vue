<template>
  <div class="product">
    <div class="product-name-rating-block">
      <div class="product-name-rating-block__title">{{ product.name }}</div>
      <div class="product-name-rating-block__article">
        Арт. {{ product.art }}
      </div>
      <ratingComp></ratingComp>
    </div>
    <div class="product-price-block">
      <div class="product-price-block__price">
        <div class="product-price-block__current-price">
          {{ product.price.current }} <span class="price">&#8399;</span>
        </div>
        <div class="product-price-block__last-price">
          {{ product.price.last }} <span class="price">&#8399;</span>
        </div>
        <img src="../assets/icons/arrow-right-swipe.svg" alt="" srcset="" />
      </div>
      <div class="product-price-block__product-shares">
        <span v-for="(item, index) in productShares">
          {{ item }}
        </span>
      </div>
    </div>
    <div class="product-parameters-block">
      <select class="product-parameters-block__select">
        <option value="" disabled selected>Выбрать размер</option>
        <option>Пункт 1</option>
        <option>Пункт 2</option>
      </select>
      <div class="product-parameters-block__determine-size">
        Oпределить размер
      </div>
    </div>
    <div class="product-buy-block">
      <productQuantity style="margin-right: 12px"></productQuantity>
      <ButtonUi style="margin-right: 4px">Добавить в корзину</ButtonUi>
      <ButtonHeart></ButtonHeart>
      <br />
      <div class="product-buy-block__buy-one-click">Купить в 1 клик</div>
    </div>

    <div class="product-description-pay-delivery-block">
      <div class="product-description-pay-delivery-block__item">
        <img src="../assets/icons/Closes.svg" alt="" srcset="" />
        <a href="/"><span>Описание товара</span></a>
      </div>
      <div class="product-description-pay-delivery-block__item">
        <img src="../assets/icons/clock.svg" alt="" srcset="" />
        <a href="/"><span>Доставка и возврат</span></a>
      </div>
      <div class="product-description-pay-delivery-block__item">
        <img src="../assets/icons/pay.svg" alt="" srcset="" />
        <a href="/"><span>Способы оплаты</span></a>
      </div>
    </div>
  </div>
</template>
<script>
import productQuantity from "./productQuantityComp.vue";
import ButtonUi from "./Ui/ButtonUi.vue";
import ButtonHeart from "./Ui/ButtonHeart.vue";
import ratingComp from "./ratingComp.vue";

export default {
  name: "ProductCardComponent",
  components: {
    productQuantity,
    ButtonUi,
    ButtonHeart,
    ratingComp,
  },

  data() {
    return {
      product: {
        name: "Пижама для девочек",
        art: "02765/46",
        price: {
          current: "800",
          last: "1 500",
        },
      },
      productShares: ["скидка -36%", "акция -20%"],
    };
  },
};
</script>
<style lang="scss" scoped>
@import url(https://fonts.googleapis.com/css?family=PT+Sans);
.price {
  font-family: "PT Sans", serif;
}

.product {
  // border: 1px dotted rgb(234, 0, 255);
  // background-color: rgb(252, 67, 212);
}

.product-name-rating-block {
  padding: 20px 0px 24px 20px;
  // width: 686px;
  // height: 136px;
  // background-color: rgb(107, 26, 26);
  &__title {
    font-weight: 600;
    font-size: 18px;
    line-height: 133%;
  }

  &__article {
    margin-top: 10px;

    font-weight: 400;
    font-size: 12px;
    line-height: 16px;
    letter-spacing: 0.04em;
    color: #828282;
  }
  &__customer-review {
  }
}

.ratingComp {
  margin-top: 15px;
}

.product-price-block {
  max-width: 686px;

  padding: 20px 0px 24px 20px;
  // height: 96px;
  // background-color: rgb(216, 125, 125);
  &__price {
    display: flex;
    align-items: center;
    // border: 1px dotted rgb(234, 0, 255);
  }
  &__current-price {
    font-weight: 700;
    font-size: 24px;
    line-height: 24px;
    letter-spacing: 0.04em;
    text-transform: uppercase;

    width: 80px;
  }

  &__last-price {
    width: 62px;

    font-weight: 400;
    font-size: 14px;
    line-height: 20px;

    letter-spacing: 0.04em;
    text-decoration-line: line-through;

    color: #828282;
  }

  &__product-shares {
    // border: 1px dotted rgb(234, 0, 255);
    margin-top: 12px;

    span {
      font-size: 13px;
      border: 1px solid rgb(0, 0, 0);
      padding: 1px 7px;
      margin-right: 9px;
      display: inline-block;
    }
  }
}

.product-parameters-block {
  // width: 686px;
  padding: 8px 0px 24px 20px;

  &__determine-size {
    margin-top: 12px;
    font-style: 14px;

    letter-spacing: 0.04em;
  }
  // height: 237px;

  &__select {
    width: 315px;
    height: 44px;

    border: 1px solid #333333;
    padding-left: 16px;

    background: url("../assets/icons/arrow down swipe.svg") no-repeat right;
    background-position: bottom 8px right 6px;
    background-color: #fff;
    -webkit-appearance: none;
    outline: 0px;
    letter-spacing: 0.04em;
  }

  &__product-quantity {
  }
}

.product-buy-block {
  max-width: 450px;
  padding: 16px 0px 24px 20px;
  display: flex;
  flex-wrap: wrap;
  // align-items: flex-start;

  &__buy-one-click {
    letter-spacing: 0.04em;
    margin-top: 12px;
    text-decoration: underline;
  }
}

.product-description-pay-delivery-block {
  padding: 30px 0px 24px 20px;

  // background-color: rgb(252, 67, 212);
  &__item {
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    span {
      padding-left: 4px;
      text-decoration-line: underline;
      letter-spacing: 0.04em;
    }
  }

  &__item:last-child {
    margin-bottom: 0px;
  }
}
</style>
