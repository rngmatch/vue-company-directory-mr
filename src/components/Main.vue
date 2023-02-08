<script setup>
import MainSearch from './MainSearch.vue'
</script>

<template>
  <div class="wrapper">
    <MainSearch />
    <h1>Hello There</h1>
  </div>
</template>

<style scoped lang="postcass">
    .wrapper {
    @apply flex flex-col container mx-auto py-4 gap-4;
}
</style>
