<script setup lang="ts">
// You can add composables or data here later
</script>

<template>
  <div>
    <!-- Hero Section -->
    <AppHero />

    <!-- Main Content Sections -->
    <AppSection />

    <!-- Features or Courses Section -->
    <div class="py-20">
      <div class="max-w-7xl mx-auto px-6">
        <!-- Optional Section Title -->
        <div class="text-center mb-16">
          <h2 class="text-3xl font-semibold text-gray-900 dark:text-white">
            អ្វីដែលអ្នកនឹងទទួលបាន
          </h2>
          <p class="text-gray-600 dark:text-gray-400 mt-3">
            រកឃើញមុខងារ និងធនធានដែលជួយអ្នកអភិវឌ្ឍជំនាញ
          </p>
        </div>
        <!-- AppCart with Style -->
        <div class="styled-cart-container">
          <AppCart />
        </div>
      </div>
    </div>
    <UPageLogos
      title="បច្ចេកវិទ្យាដែលបានប្រើ"
      marquee
      :items="[
        'i-simple-icons-github',
        'i-simple-icons-nuxt',
        'i-simple-icons-git',
        'i-simple-icons-postgresql',
        'i-simple-icons-elixir',
        'i-simple-icons-tailwindcss'
      ]"
      class="py-4"
    />
  </div>
</template>
