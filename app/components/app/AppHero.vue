<script setup lang="ts">
import type { ButtonProps } from '@nuxt/ui'

const links = ref<ButtonProps[]>([
  {
    label: 'Get started',
    to: '/docs/getting-started',
    icon: 'i-lucide-square-play'
  },
  {
    label: 'Learn more',
    to: '/docs/getting-started/theme/design-system',
    color: 'neutral',
    variant: 'subtle',
    trailingIcon: 'i-lucide-arrow-right'
  }
])
</script>

<template>
  <UPageHero
    title="ស្វាគមន៍មកកាន់ Code Sprout"
    description="វេទិកាសិក្សាកម្មវិធី និងអភិវឌ្ឍកូដឥតគិតថ្លៃ ដែលត្រូវបានបង្កើតឡើងជាពិសេសសម្រាប់ យុវជនខ្មែរ។ រៀនដោយប្រើបច្ចេកវិទ្យា Open Source មេរៀនដែលងាយយល់ គម្រោងពិតប្រាកដ និងការគាំទ្រពីសហគមន៍។
យើងជឿជាក់ថា រាល់និស្សិតខ្មែរមានសិទ្ធិទទួលបាននូវការអប់រំផ្នែកបច្ចេកវិទ្យាដែលមានគុណភាពខ្ពស់ ដើម្បីអាចរួមចំណែកអភិវឌ្ឍប្រទេសជាតិ។"
    :links="links"
  />
</template>
