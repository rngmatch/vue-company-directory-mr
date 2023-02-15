<script setup>
import { ref } from 'vue'
import { useAuth } from '@/composables/useAuth'

const { isAuthenticated } = useAuth()
const brand = ref(' RNG Company Directory')
</script>

<template>
  <nav>
    <div class="wrapper">
      <RouterLink :to="{ name: 'Home' }" class="brand">
        <span class="brand-title">{{ brand }}</span>
      </RouterLink>
      <div class="menu">
        <RouterLink :to="{ name: 'Home' }" class="menu-item">Departments</RouterLink>
        <div v-if="isAuthenticated">
          <RouterLink :to="{ name: 'Login' }" class="menu-login">Login</RouterLink>
        </div>
        <div v-else>
          <RouterLink :to="{ name: 'Home' }" class="menu-item">Settings</RouterLink>
          <RouterLink :to="{ name: 'Home' }" class="menu-logout">Logout</RouterLink>
        </div>
      </div>
    </div>
  </nav>
</template>

<style scoped lang="postcss">
nav {
  @apply flex h-20 bg-slate-900 text-slate-200;
  .wrapper {
    @apply container mx-auto flex w-full items-center justify-between;
    .brand {
      &-title {
        @apply text-2xl font-bold text-yellow-500;
      }
    }
    .menu {
      @apply flex gap-2;
      div {
        @apply py-2;
      }
      &-item {
        @apply rounded-md px-4 py-2 hover:bg-yellow-500 hover:text-slate-900;
      }
      &-login {
        @apply rounded-md bg-blue-500 px-4 py-2 text-red-100 hover:bg-blue-700 hover:font-bold hover:text-slate-900;
      }
      &-logout {
        @apply mx-2 rounded-md bg-red-500 px-4 py-2 text-red-100 hover:bg-red-700;
      }
    }
  }
}
</style>
