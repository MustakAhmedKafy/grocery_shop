<!-- ReusableButton.vue -->

<template>
  <a :href="link" :class="computedClasses"
    >{{ title }} <i class="fa-solid fa-cart-shopping"></i
  ></a>

  <!-- <ReusableButton link="cart.html" title="Add to basket" color="primary" />
    <ReusableButton link="cart.html" title="Custom Title" color="secondary" outline /> -->
</template>

<script setup>
import { defineProps, computed } from "vue";

const props = defineProps({
  link: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    default: "Add to basket",
  },
  color: {
    type: String,
    default: "primary",
  },
  outline: {
    type: Boolean,
    default: false,
  },
});

const computedClasses = computed(() => {
  return [
    "btn",
    props.outline ? `btn-outline-${props.color}` : `btn-${props.color}`,
    "p-1",
    "w-100",
    "mt-2",
  ];
});
</script>

<style lang="scss">
$primary-color: #577537;

.btn-primary {
 background-color: $primary-color !important;
 border: 0 !important;
}
</style>
