<script setup lang="ts">
// ១. រក្សាទុកបញ្ជីម៉ឺនុយជា Array (ងាយស្រួលថែមថយ ឬកែប្រែនៅទីនេះ)
const navLinks = [
  { label: 'HTML', to: '/html' },
  { label: 'CSS', to: '/css' },
  { label: 'JavaScript', to: '/javascript' },
  { label: 'Vue.js', to: '/vue' },
  { label: 'Nuxt3', to: '/nuxt3' }
]
</script>

<template>
  <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
    <div class="flex items-center gap-4" />

    <nav class="hidden md:flex items-center gap-8 text-sm font-medium">
      <NuxtLink
        v-for="link in navLinks"
        :key="link.to"
        :to="link.to"
        class="text-neutral-600 dark:text-neutral-300 hover:text-emerald-600 dark:hover:text-emerald-400 transition-colors duration-200"
      >
        {{ link.label }}
      </NuxtLink>
    </nav>

    <div class="flex items-center gap-4" />
  </div>
</template>
