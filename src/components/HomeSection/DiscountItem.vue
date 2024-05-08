<script setup>
const images = [
  { src: "./img/discount-img.jpg", alt: "discount products" },
  { src: "./img/discount-img1.jpg", alt: "discount products" },
  { src: "./img/discount-img2.jpg", alt: "discount products" },
];
</script>
<template>
  <div class="container py-4">
    <div class="row">
      <div
        class="col-lg-4 col-md-8 mt-3 mt-lg-0"
        v-for="(image, index) in images"
        :key="index"
      >
        <div class="card shadow border-0">
          <img class="card-img" :src="image.src" alt="succulent" />
          <div class="card-img-overlay text-white text-center mt-5">
            <button class="btn btn-light text-danger fw-bold display-4 rounded-pill">-30%</button>
            <h2 class="card-title">
              Delicious Cheese from<br />Selected Farms
            </h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  border-radius: 30px;
  transition: all 1s ease-out;
  img {
    border-radius: 30px;
  }
  &:hover {
    transform: translateY(-10px);
    transition: all 1s ease-out;
  }
}
</style>
