<template>
  <div v-for="item in 100" :key="item.id">page user</div>
</template>
<script setup>
definePageMeta({
  layout: "user",
});
</script>
