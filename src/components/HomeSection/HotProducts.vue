<script setup>
import Title from "../reusable/Title.vue";
const imgUrl = "./img/items-01.jpg";
</script>

<template>
  <div class="bg-color py-5">
    <div class="container">
      <Title :title="'Hot Products'" />
      <div class="row">
        <div class="col-md-3">
          <div class="card bg-white border-0 rounded-0 text-center">
            <img class="w-100" :src="imgUrl" alt="" />
            <p class="title mt-3">
              Wireless Bluetooth Headset Single Ear Lorem, ipsum dolor.
            </p>
            <div class="rating">
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
            </div>
            <p class="review">(121 review)</p>
            <p class="item-discount py-2">
              <span class="fw-bold">$8.50</span>
              <span class="discount ms-2"
                ><span class="text-decoration-line-through">$16</span> -
                50%</span
              >
            </p>
          </div>

          <!--  -->
          <div class="container">
            <div class="row justify-content-center">
             
            </div>
          </div>
        </div>
         <div class="col-lg-4 col-md-8">
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
                      <small class="text-muted">
                        Last updated 3 mins ago
                      </small>
                    </p>
                  </div>
                </div>
              </div>
      </div>
    </div>
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
    font-size: 14px;
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
