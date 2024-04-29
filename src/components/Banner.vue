<script setup></script>

<template>
  <div class="">
    <section class="main-banner">
      <div class="container col-xxl-8 px-4 py-5">
        <div class="row flex-lg-row-reverse align-items-center g-5 py-5">
          <div class="col-12 col-sm-8 col-lg-6">
            <h1 class="display-5 fw-bold lh-1 mb-3 text-dark">
              Don't Miss Out on Tasty Grocery Deals!
            </h1>
            <p class="lead text-dark">Sign Up for the Daily Newsletter</p>
            <div class="d-grid gap-2 d-md-flex justify-content-md-start">
              <div class="input-group mb-3 p-2 bg-white rounded-pill">
                <span class="input-group-text border-0 bg-transparent"
                  ><i class="fa-solid fa-envelope"></i
                ></span>
                <input
                  type="text"
                  class="form-control border-0"
                  aria-label="Amount (to the nearest dollar)"
                />
                <span class="input-group-text rounded-pill border-0 m-0"
                  >Subscribe</span
                >
              </div>
            </div>
          </div>
          <div class="col-lg-6"></div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss">
$primary-color: #577537;

.main-banner {
  .fa-envelope {
    color: $primary-color;
  }

  .form-control {
    &:focus {
      box-shadow: none;
    }
  }

  .input-group-text {
    background-color: $primary-color;
    color: #fff;
  }
}

.main-banner {
  background: rgba(0, 0, 0, 0) url("./img/main-banner.jpg") repeat scroll 0 0 /
    cover;
  height: 70vh;
  position: relative;
  width: 100%;
  z-index: 1;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
