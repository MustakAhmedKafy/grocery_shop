<script setup>
import Title from "../reusable/Title.vue";
const HalalFood = "./img/Hala_Food.jpg";

const images = [
  { src: "./img/Fast_Food.jpg", alt: "Fast Food" },
  { src: "./img/Oil.jpg", alt: "Oil" },
  { src: "./img/Vegetable.jpg", alt: "Vegetable" },
  { src: "./img/Dairy_Item.jpg", alt: "Dairy Item" },
];
</script>

<template>
  <section class="product-item pb-5">
   <Title :title="'Top Categories'"></Title>
    <div class="container pt-4">
      <div class="row">
        <div class="col-md-6 mt-3">
          <a href="shop.html">
            <div class="img-wrapper shadow">
              <div class="inner-img">
                <img class="w-100" :src="HalalFood" alt="" />
              </div>
            </div>
          </a>
        </div>
        <div class="col-md-6 mt-2">
          <div class="row">
            <div
              v-for="(image, index) in images"
              :key="index"
              class="col-md-6 mt-2"
            >
              <a href="shop.html">
                <div class="img-wrapper shadow">
                  <div class="inner-img">
                    <img class="w-100" :src="image.src" :alt="image.alt" />
                  </div>
                </div>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.img-wrapper {
  width: 100%;
  overflow: hidden;
  border-radius: 7px;

  .inner-img {
    transition: 0.3s;

    &:hover {
      transform: scale(1.1);
    }
  }

  img {
    width: 100%;
    border-radius: 7px;
    object-fit: cover;
  }
}
</style>
