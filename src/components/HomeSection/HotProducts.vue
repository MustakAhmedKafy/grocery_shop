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
  <div class="bg-color py-5">
    <div class="container">
      <Title :title="'Hot Products'" />
      <div class="row">
        <div class="col-md-3" v-for="(item, index) in hotItems" :key="index">
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
        <!-- <div class="col-lg-4 col-md-8" >
          <div class="card shadow">
            <img
              class="card-img"
              src="https://source.unsplash.com/1600x900/?succulent,green,dark,table"
              alt="succulent"
            />
            <div class="card-img-overlay text-white">
              <h5 class="card-title">Card Title</h5>
              <p class="card-text">lorem ipsum dolor set amet</p>
            </div>
            <div class="card-body">
              <h4 class="card-title">Another Title</h4>
              <p class="card-text">
                <small class="text-muted"> Last updated 3 mins ago </small>
              </p>
            </div>
          </div>
        </div> -->
      </div>
    </div>
  </div>
</template>
