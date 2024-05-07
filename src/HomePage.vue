<script setup>
import Banner from "./components/HomeSection/Banner.vue";
import ItemCategories from "./components/HomeSection/ItemCategories.vue";
import ShopItem from "./components/HomeSection/ShopItem.vue";
import Brands from "./components/HomeSection/Brands.vue";
import HotProducts from "./components/HomeSection/HotProducts.vue";
import DiscountItem from "./components/HomeSection/DiscountItem.vue";
</script>

<template>
  <div>
    <Banner />
    <ItemCategories />
    <ShopItem />
    <DiscountItem />
    <HotProducts />
    <Brands />
  </div>
</template>
<style lang="scss">
.bg-color {
  background-color: #f0feee;
}
</style>
