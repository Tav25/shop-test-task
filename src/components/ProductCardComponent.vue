<template>
  <div>
    <div class="product-name-rating-block">
      <div class="product-name-rating-block__title">Пижама для девочек</div>
      <div class="product-name-rating-block__article">Арт. 02765/46</div>
      <div class="product-name-rating-block__customer-review customer-review">
        <span>Отзывы</span>
        <div class="customer-review__stars">*****</div>
        <div class="customer-review__link-review">14 отзывов ></div>
      </div>
    </div>
    <div class="product-price-block">
      <div class="product-price-block__price"></div>
      <div class="product-price-block__product-shares"></div>
    </div>
    <div class="product-parameters-block">
      <select>
        <option>Пункт 1</option>
        <option>Пункт 2</option>
      </select>
      <span>определить размер</span>
      <div class="product-parameters-block__product-quantity product-quantity">
        <div class="product-quantity__up">+</div>
        <div class="product-quantity__quantity">1</div>
        <div class="product-quantity__down">-</div>
      </div>

      <div></div>
      <span>купить в один клик</span>
    </div>
    <div class="product-description-pay-delivery-block">
      <div class="product-description-pay-delivery-block__description"></div>
      <div class="product-description-pay-delivery-block__pay"></div>
      <div class="product-description-pay-delivery-block__delivery"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ProductCardComponent",
};
</script>
<style lang="scss" scoped>
.product-name-rating-block {
  width: 686px;
  height: 136px;
  background-color: rgb(107, 26, 26);
}

.product-price-block {
  width: 686px;
  height: 96px;
  background-color: rgb(216, 125, 125);
}

.product-parameters-block {
  width: 686px;
  height: 237px;
  background-color: rgb(23, 158, 118);
  &__product-quantity {
  }
}

.product-quantity {
  width: 145px;
  height: 44px;

  display: flex;
  justify-content: space-between;
  /* Gray 6 */

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
    background-color: rgb(138, 68, 68);
  }

  &__up {
    flex: 0 1 33.3%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

.product-description-pay-delivery-block {
  width: 686px;
  height: 132px;
  background-color: rgb(252, 67, 212);
}
</style>
