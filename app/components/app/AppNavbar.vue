<script setup lang="ts">
// ១. រក្សាទុកបញ្ជីម៉ឺនុយជា Array (ងាយស្រួលថែមថយ ឬកែប្រែនៅទីនេះ)
const categories = [
  {
    name: 'Frontend Foundation',
    items: [
      { label: 'HTML', to: '/html', icon: 'i-heroicons-code-bracket' },
      { label: 'CSS', to: '/css', icon: 'i-heroicons-paint-brush' },
      { label: 'JavaScript', to: '/javascript', icon: 'i-heroicons-bolt' },
      { label: 'TypeScript', to: '/typescript', icon: 'i-heroicons-document-check' },
      { label: 'DOM Manipulation', to: '/dom', icon: 'i-heroicons-cursor-arrow-rays' }
    ]
  },
  {
    name: 'Advanced Ecosystem',
    items: [
      { label: 'Vue.js', to: '/vue', icon: 'i-heroicons-rectangle-group' },
      { label: 'Nuxt 3', to: '/nuxt3', icon: 'i-heroicons-squares-2x2' },
      { label: 'Tailwind CSS', to: '/tailwind', icon: 'i-heroicons-sparkles' },
      { label: 'Pinia (State)', to: '/state', icon: 'i-heroicons-arrows-right-left' },
      { label: 'Vue Router', to: '/router', icon: 'i-heroicons-map' }
    ]
  },
  {
    name: 'Backend & Database',
    items: [
      { label: 'Node.js', to: '/nodejs', icon: 'i-heroicons-server' },
      { label: 'Express.js', to: '/express', icon: 'i-heroicons-cpu-chip' },
      { label: 'PostgreSQL', to: '/postgresql', icon: 'i-heroicons-circle-stack' },
      { label: 'MongoDB', to: '/mongodb', icon: 'i-heroicons-cube' },
      { label: 'REST APIs', to: '/apis', icon: 'i-heroicons-cloud-arrow-up' }
    ]
  },
  {
    name: 'DevOps & Deployment',
    items: [
      { label: 'Git & GitHub', to: '/git', icon: 'i-heroicons-share' },
      { label: 'Docker', to: '/docker', icon: 'i-heroicons-square-3-stack-3d' },
      { label: 'Vercel / Netlify', to: '/deploy', icon: 'i-heroicons-rocket-launch' },
      { label: 'Web Security', to: '/security', icon: 'i-heroicons-shield-check' },
      { label: 'Testing (Vitest)', to: '/testing', icon: 'i-heroicons-beaker' }
    ]
  }
]
</script>

<template>
  <div class="max-w-7xl mx-auto px-6 py-2 border-b border-gray-200 dark:border-gray-800">
    <nav class="flex items-center gap-8 overflow-x-auto scrollbar-none">
      <div
        v-for="category in categories"
        :key="category.name"
        class="flex items-center gap-3 border-r last:border-0 border-gray-200 dark:border-gray-800 pr-6 last:pr-0"
      >
        <span class="text-xs font-bold uppercase tracking-wider text-neutral-400 dark:text-neutral-500 hidden 2xl:inline whitespace-nowrap">
          {{ category.name }}
        </span>

        <div class="flex items-center gap-2">
          <NuxtLink
            v-for="topic in category.items"
            :key="topic.to"
            :to="topic.to"
            class="flex items-center gap-1.5 px-3 py-1.5 text-sm font-medium rounded-lg transition-all duration-200 whitespace-nowrap"
            active-class="bg-emerald-50 dark:bg-emerald-950/40 text-emerald-600 dark:text-emerald-400 font-semibold"
            inactive-class="text-neutral-600 dark:text-neutral-400 hover:bg-neutral-50 dark:hover:bg-zinc-800/50 hover:text-neutral-900 dark:hover:text-white"
          >
            <UIcon
              :name="topic.icon"
              class="w-4 h-4 shrink-0"
            />
            <span>{{ topic.label }}</span>
          </NuxtLink>
        </div>
      </div>
    </nav>
  </div>
</template>
