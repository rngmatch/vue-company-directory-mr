<template>
  <div class="wrapper">
    <input type="text" placeholder="Search Staff Member" class="search" />
  </div>
</template>

<style scoped lang="postcss">
.wrapper {
  @apply relative flex w-full items-stretch;
  .search {
    @apply px-3 py-4 placeholder-slate-400;
  }
}
</style>
