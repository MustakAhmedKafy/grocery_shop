<script setup>
import PrimaryButton from "./PrimaryButton.vue"
const props = defineProps([
  "offerHeader",
  "offer",
  "image",
  "extraOff",
  "extraOffDiscount",
  "title",
  "collectionPrice",
  "collectionOfferPrice",
  "deliveryPrice",
  "deliveryOfferPrice",
]);
</script>

<template>
  <div class="card position-relative border-0 shadow">
    <div
      v-if="offerHeader"
      class="card-header border-0 d-flex justify-content-between rounded-top"
    >
      <p class="text-white m-0">{{ offer }}</p>
      <span class="text-white"><i class="fa-solid fa-heart"></i></span>
    </div>
    <img :src="image" class="card-img-top rounded-top" alt="..." />
    <div class="card-body">
      <h6 v-if="extraOff" class="text-center extra-off text-white extraOff">
        Extra
        <span class="fw-bold"
          ><i class="fa-solid fa-sterling-sign"></i>{{ extraOffDiscount }}</span
        >
        OFF
      </h6>
      <h6 class="card-title text-center">{{ title }}</h6>
      <div class="d-flex justify-content-between py-1">
        <span class="rounded-pill price"
          ><del>Col: £{{ collectionPrice }}</del></span
        >
        <span class="rounded-pill price"
          ><del>Del: £{{ deliveryPrice }}</del></span
        >
      </div>
      <div class="d-flex justify-content-between py-1">
        <span class="rounded-pill price2"
          >Col: £{{ collectionOfferPrice }}</span
        >
        <span class="rounded-pill price2">Del: £{{ deliveryOfferPrice }}</span>
      </div>
     <PrimaryButton link="#" title="Add to basket" color="primary"/>
    </div>
  </div>
</template>

<style lang="scss">
$primary-color: #577537;
.card {
  .price {
    background-color: #e1e1e1;
    padding: 0px 8px;
    font-size: 13px;
    color: #000;
  }

  .price2 {
    background-color: #ffc107;
    padding: 0px 7px;
    font-size: 13px;
    color: #000;
  }

  h6 {
    font-size: 14px;
    color: #000;
  }

  // .accordion-body {
  //   padding: 0px !important;

  //   .shop-sub-menu {
  //     padding: 10px 10px 10px 30px;
  //   }

  //   .shop-sub-menu-2 {
  //     padding-left: 40px;
  //   }
  // }

  // .accordion {
  //   border: 0px !important;
  // }

  // .accordion-item {
  //   border: 0px !important;
  // }

  // .accordion-item:first-of-type .accordion-button {
  //   border-radius: 0px;
  //   border: 0px !important;
  // }

  // .accordion-button {
  //   background-color: transparent;
  //   color: $primary-color;
  // }

  // .accordion-collapse {
  //   border: 0px !important;
  // }

  // .collapse {
  //   border: 0px !important;
  // }

  // .list-group-item:last-child {
  //   border-bottom-right-radius: 0;
  //   border-bottom-left-radius: 0;
  // }

  // .list-group-item:first-child {
  //   border-top-left-radius: 0;
  //   border-top-right-radius: 0;
  // }

  // .list-group {
  //   border: 0px !important;
  // }

  // .list-group-item {
  //   border: 0px !important;
  // }

  // acordian end

  img {
    border-radius: 0px;
  }

  .card-header {
    position: absolute;
    top: 0;
    width: 100%;
    padding: 6px 12px;
    background-color: #ff6666;
  }

  .extra-off {
    position: absolute;
    top: 170px;
    left: 14px;
    background-color: #00a967;
    padding: 5px 10px 7px 10px;
    border-radius: 50px;
  }

  .product-collection-price {
    padding: 10px 0px;
  }
}
</style>
