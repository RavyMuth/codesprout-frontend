<script setup>
const navMenuLinks = [
  { label: 'Home', to: '/' },
  { label: 'About', to: '/abouts' },
  { label: 'Contact', to: '/contact' },
  { label: 'Project', to: '/project' }
]
</script>

<template>
  <header class="p-4 flex justify-between items-center max-w-7xl mx-auto border-b border-gray-200 dark:border-gray-800 ">
    <div class="flex items-center gap-3">
      <div class="w-8 h-8 bg-emerald-500 rounded-xl flex items-center justify-center text-white text-xl">
        🌱
      </div>
      <span class="font-bold text-2xl text-gray-900 dark:text-white">CodeSprout</span>
    </div>

    <div class="flex items-center gap-6">
      <NuxtLink
        v-for="link in navMenuLinks"
        :key="link.to"
        :to="link.to"
        class="hover:text-emerald-600 dark:hover:text-emerald-400 transition-colors"
      >
        {{ link.label }}
      </NuxtLink>
    </div>

    <div class="flex items-center gap-4">
      <UColorModeButton class="hover:text-emerald-600 dark:hover:text-emerald-400" />
      <button
        class="px-5 py-2 text-sm font-medium border border-gray-300 dark:border-zinc-700 rounded-xl transition"
        @click="login"
      >
        Log in
      </button>
      <button
        class="px-5 py-2 text-sm font-medium bg-emerald-600 text-white rounded-xl hover:bg-emerald-500 transition"
        @click="join"
      >
        Join Free
      </button>
    </div>
  </header>
</template>
