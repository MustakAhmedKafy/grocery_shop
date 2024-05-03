<script setup>
import ProductCard from "../reusable/ProductCard.vue";
const productsItem = [
  {
    offerHeader: true,
    offer: "Offer end 29/04",
    image: "./img/items-01.jpg",
    extraOff: true,
    extraOffDiscount: 5,
    title: "Product 1 Title",
    collectionPrice: 30,
    collectionOfferPrice: 25,
    deliveryPrice: 3,
    deliveryOfferPrice: 1,
  },
  {
    offerHeader: false,
    offer: "Offer end ",

    image: "./img/items-01.jpg",
    extraOff: false,
    extraOffDiscount: 0,
    title: "Product 2 Title",
    collectionPrice: 70,
    collectionOfferPrice: 55,
    deliveryPrice: 7,
    deliveryOfferPrice: 5,
  },
];
</script>
<template>
  <section>
    <div class="container py-5">
      <div class="row">
        <div class="col-md-3" v-for="items in productsItem" :key="index">
          <ProductCard
            :offerHeader="items.offerHeader"
            :offer="items.offer"
            :image="items.image"
            :extraOff="items.extraOff"
            :extraOffDiscount="items.extraOffDiscount"
            :title="items.title"
            :collectionPrice="items.collectionPrice"
            :collectionOfferPrice="items.collectionOfferPrice"
            :deliveryPrice="items.deliveryPrice"
            :deliveryOfferPrice="items.deliveryOfferPrice"
          />
        </div>
      </div>
    </div>
  </section>
</template>
