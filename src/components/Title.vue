<script setup>
const props = defineProps(["title"]);
</script>
<template>
  <div>
    <h2 class="pb-4 text-center">{{ title }}</h2>
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
