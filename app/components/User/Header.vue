<template>
  <header class="fixed inset-x-0 top-0 z-50 border-t-[10px] border-[#284549] bg-white shadow-[0_10px_30px_rgba(15,23,42,0.08)]">
    <div class="mx-auto flex min-h-[120px] w-full max-w-7xl items-center justify-between gap-6 px-4 py-5 sm:px-6 lg:px-8">
      <div class="flex min-w-0 items-center gap-4">
        <img :src="headerLogo" :alt="unitStore.name" class="h-auto w-[220px] max-w-full sm:w-[280px] lg:w-[360px]" />
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
const unitStore = useUnitStore();
const headerLogo = computed(() => unitStore.logoFull || unitStore.logo);
</script>
