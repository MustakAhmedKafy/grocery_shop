<script setup>
const socialMedia = [
  { icon: "fa-facebook-f", link: "#" },
  { icon: "fa-instagram", link: "#" },
  { icon: "fa-whatsapp", link: "#" },
  { icon: "fa-youtube", link: "#" },
];
</script>

<template>
  <section class="header-top d-none d-lg-block py-3">
    <div class="container">
      <div class="d-flex justify-content-between">
        <div>
          <span
            ><i class="fa-regular fa-clock"></i> Delivery on Next Day from 10:00
            AM to 08:00 PM</span
          >
        </div>

        <div class="header-social">
          <span
            ><i class="fa-solid fa-headphones-simple"></i> +1 900 777525</span
          >
          <div class="social d-inline">
            <span v-for="media in socialMedia" :key="media.icon">
              <i
                :class="['fa-brands', media.icon]"
                :aria-label="media.icon"
              ></i>
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.header-top {
  .header-social span {
    padding: 0px 5px;
    color: #577537;
  }
  .fa-clock {
    color: #577537;
  }
}
</style>
