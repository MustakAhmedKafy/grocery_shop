<script setup>
import HotProductsCard from "../reusable/HotProductsCard.vue";

import Title from "../reusable/Title.vue";
const imgUrl = "./img/items-01.jpg";
const hotItems = [
  {
    image: "./img/items-01.jpg",
    title: "Item 1",
    rating: 5,
    review: 121,
    price: 8.5,
    originalPrice: 16.6,
    discount: 50,
  },
  {
    image: "./img/items-01.jpg",
    title: "Item 1",
    rating: 3,
    review: 121,
    price: 8.5,
    originalPrice: 16.6,
    discount: 50,
  },
];
</script>

<template>
  <div class="bg-color pb-5">
    <Title :title="'Hot Products'" />
    <div class="container pt-4">
      <div class="row">
        <div class="col-md-3 mt-3" v-for="(item, index) in hotItems" :key="index">
          <HotProductsCard
            :image="item.image"
            :title="item.title"
            :rating="item.rating"
            :review="item.review"
            :price="item.price"
            :originalPrice="item.originalPrice"
            :discount="item.discount"
          />
        </div>
      </div>
    </div>
  </div>
</template>
