<script setup>
const props = defineProps({
  showCart: Boolean,
});

const emit = defineEmits(["close"]);

function closeCart() {
  emit("close");
}
</script>

<template>
  <div v-show="showCart" class="header-cart">
    <!--  -->
    <div class="menu px-3 text-white">
      <a class="btn menu-click pe-4 my-2" @click="closeCart">
        <i class="fa fa-times"></i>
      </a>
      <h5 class="py-3">Shopping Cart 2</h5>
      <div class="border-bottom d-flex justify-content-between pb-2">
        <div>
          <p class="m-0">Sparkling Water</p>
          <p class="m-0">1000ml</p>
        </div>
        <div><span class="mt-1">1 * £600.00</span></div>
      </div>
      <div class="border-bottom d-flex justify-content-between pb-2">
        <div>
          <p class="m-0">Sparkling Water</p>
          <p class="m-0">1000ml</p>
        </div>
        <div><span class="mt-1">1 * £600.00</span></div>
      </div>
      <div class="d-flex justify-content-between mt-2">
        <h6>Sub Total</h6>
        <h6>£1200.00</h6>
      </div>
      <a href="cart.html">
        <button class="btn btn-light w-100 mt-2">
          View Cart <i class="fa-solid fa-cart-shopping"></i></button
      ></a>
      <a href="checkout.html">
        <button class="btn btn-outline-warning w-100 mt-2">
          Checkout <i class="fa-solid fa-check"></i></button
      ></a>
    </div>
  </div>
</template>

<style lang="scss">
$primary-color: #577537;
.header-cart {
  background-color: $primary-color;
  top: 0;
  width: 380px;
  height: 100vh;
  position: fixed;
  right: 0px;
  transition: all 0.2s ease-out;
  z-index: 9999;
  // drawer
  .menu {
    h5 {
      color: #fff;
    }
    .menu-click {
      color: white;
      .fa {
        margin-left: 8px;
      }
    }

   
  }

  // .fa-solid {
  //   color: #fff;
  //   font-size: 20px;
  // }
}
</style>
