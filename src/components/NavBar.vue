<script setup>
import { ref } from 'vue'
const brand = ref('RNG Company Directory')
</script>

<template>
  <nav>
    <div class="wrapper">
      <div class="brand">
        <span class="brand-title">{{ brand }}</span>
      </div>
      <div class="menu">
        <a href="#" class="menu-item">Depratments </a>
        <a href="#" class="menu-item">Settings </a>
        <a href="#" class="menu-login">Logout </a>
      </div>
    </div>
  </nav>
</template>

<style scoped lang="postcss">
nav {
  @apply flex h-20 bg-slate-900 text-slate-200;
  .wrapper {
    @apply flex·container·mx-auto w-full items-center justify-between;
    .brand {
      &-title {
        @apply text-2xl font-bold text-yellow-500;
      }
    }
    .menu {
      @apply flex gap-2;
      &-item {
        @apply rounded-md px-4 py-2 hover:bg-yellow-700 hover:text-slate-900;
      }
      &-login {
        @apply rounded-md bg-red-500 px-4 py-2 hover:bg-red-700 hover:font-bold hover:text-slate-900;
      }
    }
  }
}
</style>
