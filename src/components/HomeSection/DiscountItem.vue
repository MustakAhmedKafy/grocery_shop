<script setup>
const images = [{ src: "./img/discount-img.jpg", alt: "discount products" }];
</script>
<template>
  <div class="container py-4">
    <div class="row">
      <div
        class="col-lg-4 col-md-8"
        v-for="(image, index) in images"
        :key="index"
      >
        <div class="card shadow border-0">
          <img class="card-img" :src="image.src" alt="succulent" />
          <div class="card-img-overlay text-white">
            <h5 class="card-title">Card Title</h5>
            <p class="card-text">lorem ipsum dolor set amet</p>
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
