<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
import MainSearch from './MainSearch.vue'
</script>

<template>
  <div class="wrapper">
    <MainSearch />
    <h1>Hello There</h1>
  </div>
</template>

<style scoped lang="postcss">
.wrapper {
  @apply flex flex-col gap-4 py-4;
}
</style>
