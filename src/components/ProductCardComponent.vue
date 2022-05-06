<template>
  <div class="product">
    <div class="product-name-rating-block">
      <div class="product-name-rating-block__title">Пижама для девочек</div>
      <div class="product-name-rating-block__article">Арт. 02765/46</div>
      <div class="product-name-rating-block__customer-review customer-review">
        <span>Отзывы</span>
        <span class="customer-review__stars">
          <img src="../assets/icons/row.png" alt="" srcset="" />
        </span>
        <span class="customer-review__link-review">14 отзывов </span>
        <img src="../assets/icons/arrow-right-swipe.svg" alt="" srcset="" />
      </div>
    </div>
    <div class="product-price-block">
      <div class="product-price-block__price">
        <div class="product-price-block__current-price">800 ₽</div>
        <div class="product-price-block__last-price">1500 ₽</div>
        <img src="../assets/icons/arrow-right-swipe.svg" alt="" srcset="" />
      </div>
      <div class="product-price-block__product-shares">
        <span>скидка -36%</span><span>акция -20%</span>
      </div>
    </div>
    <div class="product-parameters-block">
      <select>
        <option>Пункт 1</option>
        <option>Пункт 2</option>
      </select>
      <span>определить размер</span>
      <div style="display: flex">
        <productQuantity style="margin-right: 12px"></productQuantity>
        <ButtonUi style="margin-right: 4px">Добавить в корзину</ButtonUi>
        <ButtonHeart></ButtonHeart>
      </div>

      <span>купить в один клик</span>
    </div>
    <div class="product-description-pay-delivery-block">
      <div class="product-description-pay-delivery-block__item">
        <img src="../assets/icons/Closes.svg" alt="" srcset="" />
        <span>Описание товара</span>
      </div>
      <div class="product-description-pay-delivery-block__item">
        <img src="../assets/icons/clock.svg" alt="" srcset="" />
        <span>Доставка и возврат</span>
      </div>
      <div class="product-description-pay-delivery-block__item">
        <img src="../assets/icons/pay.svg" alt="" srcset="" />
        <span>Способы оплаты</span>
      </div>
    </div>
  </div>
</template>
<script>
import productQuantity from "./productQuantityComp.vue";
import ButtonUi from "./Ui/ButtonUi.vue";
import ButtonHeart from "./Ui/ButtonHeart.vue";

export default {
  name: "ProductCardComponent",
  components: {
    productQuantity,
    ButtonUi,
    ButtonHeart
  },
};
</script>
<style lang="scss" scoped>
.product {
  // border: 1px dotted rgb(234, 0, 255);
}

.product-name-rating-block {
  // width: 686px;
  // height: 136px;
  // background-color: rgb(107, 26, 26);
  &__title {
    font-weight: 600;
    font-size: 18px;
    line-height: 133%;
  }

  &__article {
    font-weight: 400;
    font-size: 12px;
    line-height: 16px;
    letter-spacing: 0.04em;
    color: #828282;
  }
  &__customer-review {
  }
}

.customer-review {
  width: 100%;
  display: flex;
  align-items: center;

  &__stars {
  }

  &__link-review {
  }
}

.product-price-block {
  width: 686px;
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
  }

  &__last-price {
    font-weight: 400;
    font-size: 14px;
    line-height: 20px;

    letter-spacing: 0.04em;
    text-decoration-line: line-through;

    color: #828282;
  }

  &__product-shares {
    // border: 1px dotted rgb(234, 0, 255);

    span {
      border: 1px solid rgb(0, 0, 0);
      padding: 4px 8px;
      margin-right: 9px;
      display: inline-block;
    }
  }
}

.product-parameters-block {
  width: 686px;
  // height: 237px;

  select {
    width: 315px;
    height: 44px;

    border: 1px solid #333333;
    padding-left: 16px;

    background: url("../assets/icons/arrow-right-swipe.svg") no-repeat right
      #ddd;
    background-color: #fff;
    -webkit-appearance: none;
    outline: 0px;
    // background-position-x: 244px;
  }
  // background-color: rgb(23, 158, 118);
  &__product-quantity {
  }
}

.product-description-pay-delivery-block {
  width: 686px;
  height: 132px;

  // background-color: rgb(252, 67, 212);
  &__item {
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    span {
      padding-left: 4px;
      text-decoration-line: underline;
    }
  }

  &__item:last-child {
    margin-bottom: 0px;
  }
}
</style>
