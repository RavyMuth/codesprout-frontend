<script setup>
const title = 'Nuxt Starter Template'
const description = 'A production-ready starter template powered by Nuxt UI. Build beautiful, accessible, and performant applications in minutes, not hours.'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: 'https://nuxt.com',
  twitterCard: 'summary_large_image'
})
</script>

<template>
  <div id="app">
    <AppHeader />

    <AppNavbar />

    <UMain>
      <NuxtPage />
    </UMain>

    <AppFooter />
  </div>
</template>
