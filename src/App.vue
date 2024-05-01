<script setup>
import BannerVue from "./components/Banner.vue";
import Navbar from "./components/Navbar.vue";
import Banner from "./components/Banner.vue";
import ProductItem from "./components/ProductItem.vue";
import Brands from "./components/Brands.vue";
import Footer from "./components/Footer.vue";
import ProductCard from "./components/ProductCard.vue";
import HotProducts from "./components/HotProducts.vue";
</script>

<template>
  <div>
    <Navbar />
    <Banner />
    <ProductItem />
    <ProductCard />
    <HotProducts />
    <Brands />
    <Footer />
  </div>
</template>

<style lang="scss">
.bg-color {
  background-color: #f0feee;
}
</style>
