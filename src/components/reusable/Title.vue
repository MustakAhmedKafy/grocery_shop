<script setup>
const props = defineProps(["title"]);
</script>
<template>
  <div class="pt-5">
    <h2 class=" text-center">{{ title }}</h2>
  </div>
</template>
<style lang="scss" scoped>
h2 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  font-weight: 500;
  line-height: 1.2;
}
</style>
