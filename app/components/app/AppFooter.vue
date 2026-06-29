<script setup>
const footerItems = [
  [
    { label: 'Privacy Policy', to: '/privacy', icon: 'i-heroicons-shield-check' },
    { label: 'Terms of Service', to: '/terms' },
    { label: 'Contact', to: '/contact' }
  ]
]
</script>

<template>
  <footer class="bg-gray-50 dark:bg-gray-900 border-t border-gray-200 dark:border-gray-800 transition-colors duration-200">
    <div class="max-w-7xl mx-auto px-4 py-8 sm:px-6 lg:px-8">
      <div class="flex flex-col sm:flex-row justify-between items-center gap-4">
        <div class="text-center sm:text-left">
          <p class="text-sm text-neutral-500 dark:text-neutral-400">
            &copy; {{ new Date().getFullYear() }} CodeSprout. All rights reserved.
          </p>
        </div>
        <UNavigationMenu
          :items="footerItems"
          variant="link"
          color="primary"
        />
      </div>
    </div>
  </footer>
</template>
