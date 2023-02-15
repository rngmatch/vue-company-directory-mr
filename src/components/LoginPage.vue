<script setup>
import { useAuth } from '@/composables/useAuth'
const { login } = useAuth()
</script>

<template>
  <form class="login-form" @submit="logUserIn">
    <input type="text" placeholder="Username" />
    <input type="password" placeholder="Password" />
    <button type="submit" class="bg-green-500 px-4 py-2" @click="login('admin', 'admin')">Log in</button>
  </form>
</template>

<style scoped lang="postcss">
.login-form {
  @apply mx-auto mt-80 flex max-w-lg flex-col gap-4 rounded-md bg-white p-8 shadow-lg;
  & input {
    @apply rounded-md px-4 py-2 text-xl ring-1 ring-slate-300;
  }
}
</style>
