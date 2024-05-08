<script setup>
import Title from "../reusable/Title.vue";
const brands = [
  { src: "./img/Amul_dairy_logo.png", alt: "Amul_dairy_logo" },
  { src: "./img/Coke.jpg", alt: "Coke.jpg" },
  {
    src: "./img/vadilal-ice-cream-logo.png",
    alt: "vadilal-ice-cream-logo.png",
  },
  { src: "./img/Laila-Logo-01-Copy-1.png", alt: "Laila-Logo-01-Copy-1.png" },
  { src: "./img/Haldiram-Logo-Vector.png", alt: "Haldiram-Logo-Vector.png" },
  {
    src: "./img/Parle_Products-Logo.wine.svg",
    alt: "Parle_Products-Logo.wine.svg",
  },
  // { src: "", alt: "" },
];
</script>
<template>
  <section class="featured-brands pb-5">
    <Title :title="'Featured Brands'" />
    <div class="container">
      <div class="row justify-content-center">
        <div
          v-for="(brand, index) in brands"
          :key="index"
          class="col-lg-2 col-md-4 col-6 mt-3"
        >
          <a href="#">
            <div class="card p-2 shadow border-0">
              <img class="w-100" :src="brand.src" :alt="brand.alt" />
            </div>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss" scoped>
.featured-brands {
  img {
    width: 300px;
    height: 100px;
    object-fit: contain;
  }
}
</style>
