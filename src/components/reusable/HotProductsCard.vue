<script setup>
import Rating from "../reusable/Rating.vue";
const props = defineProps([
  "image",
  "title",
  "rating",
  "review",
  "price",
  "originalPrice",
  "discount",
]);
</script>

<template>
  <div class="card bg-white border-0 rounded-0 text-center">
    <img class="w-100" :src="image" alt="" />
    <p class="title mt-3">
      {{ title }}
    </p>
    <div class="rating">
      <Rating :rating="rating"/>
    </div>
    <p class="review">({{ review }} review)</p>
    <p class="item-discount py-2">
      <span class="fw-bold">${{ price }}</span>
      <span class="discount ms-2"
        ><span class="text-decoration-line-through">${{ originalPrice }}</span>
        - {{ discount }}%</span
      >
    </p>
  </div>
</template>

<style lang="scss">
$primary-color: #577537;
.card {
  .d-flex {
    p {
      font-weight: 600;
      font-size: 14px;
    }
  }

  .title {
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
    font-size: 16px;
    font-weight: 600;
  }

  .rating {
    .fa-star {
      color: #ffd800;
      font-size: 14px;
    }
  }

  .review {
    font-size: 14px;
    color: #676e6e;
  }

  .discount {
    font-size: 14px;
  }

  .fw-bold {
    font-size: 18px;
  }

  .owl-carousel .owl-next {
    position: absolute;
    top: 40%;
    transform: translateY(-50%);
    background-color: #fff !important;
    color: #000 !important;
    font-size: 0.8em !important;
    width: 30px;
    height: 30px;
    border-radius: 100% !important;
    font-weight: bold;
    padding: 10px !important;
    text-align: center;
    box-shadow: 0px 0px 10px 0px #000;
    right: 0;
    border: 1px solid #dddfdf;
  }

  .owl-carousel .owl-prev {
    position: absolute;
    top: 40%;
    transform: translateY(-50%);
    background-color: #fff !important;
    color: #000 !important;
    font-size: 0.8em !important;
    width: 30px;
    height: 30px;
    border-radius: 100% !important;
    font-weight: bold;
    padding: 10px !important;
    text-align: center;
    box-shadow: 0px 0px 10px 0px #000;
    left: 0;
    border: 1px solid #dddfdf;
  }

  .owl-theme .owl-nav {
    margin-top: 0px !important;
  }
}
</style>
