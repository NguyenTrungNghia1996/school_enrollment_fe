<template>
  <footer class="relative mt-24 bg-[#0f2b57] text-white">
    <div class="absolute left-1/2 top-0 z-10 h-24 w-24 -translate-x-1/2 -translate-y-1/2 rounded-full border-[6px] border-white/10 bg-[#234b96] p-3 shadow-[0_15px_35px_rgba(15,43,87,0.45)]">
      <img :src="unitStore.logo" :alt="unitStore.name" class="h-full w-full object-contain" />
    </div>

    <div class="mx-auto max-w-7xl px-4 pb-6 pt-24 sm:px-6 lg:px-8">
      <div class="grid gap-8 border-b border-white/10 pb-8 text-sm sm:grid-cols-2 lg:grid-cols-[1fr_auto_1fr] lg:items-start">
        <div class="space-y-4">
          <div class="flex flex-wrap gap-x-8 gap-y-2 text-sm font-medium uppercase tracking-wide text-white/90">
            <a href="/" class="transition hover:text-[#ffd36b]">Trang chủ</a>
            <a href="#" class="transition hover:text-[#ffd36b]">Cổng khảo thí</a>
          </div>

          <div class="space-y-2 leading-7 text-white/95">
            <p class="text-base font-semibold uppercase">
              {{ unitStore.name }}
            </p>
            <p>Địa chỉ: {{ unitStore.address }}</p>
            <p>Email: {{ unitStore.email }}</p>
            <p>Điện thoại: {{ unitStore.phone }}</p>
          </div>
        </div>

        <div class="flex items-center justify-center text-center text-sm text-white/80">
          <p>Bản quyền © {{ currentYear }} {{ unitStore.name }}</p>
        </div>

        <div class="space-y-4 lg:text-right">
          <div class="flex flex-wrap gap-x-8 gap-y-2 text-sm font-medium uppercase tracking-wide text-white/90 lg:justify-end">
            <a href="#" class="transition hover:text-[#ffd36b]">Truyền thông</a>
            <a href="#" class="transition hover:text-[#ffd36b]">Tư vấn</a>
          </div>

          <div class="space-y-2 text-white/95">
            <p class="text-base font-semibold uppercase">Thống kê truy cập</p>
            <p>Đang truy cập: 0</p>
          </div>
        </div>
      </div>

      <div class="pt-5 text-center text-sm text-white/80">All Rights Reserved</div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const unitStore = useUnitStore();
const currentYear = new Date().getFullYear();
</script>
