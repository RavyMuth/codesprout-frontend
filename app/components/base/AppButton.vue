<script setup lang="ts">
interface Props {
  label?: string
  to?: string
  icon?: string
  color?: 'primary' | 'secondary' | 'success' | 'info' | 'warning' | 'error' | 'neutral'
  variant?: 'link' | 'solid' | 'outline' | 'ghost' | 'soft' | 'subtle'
  size?: 'xs' | 'sm' | 'md' | 'lg' | 'xl'
  loading?: boolean
  disabled?: boolean
}

withDefaults(defineProps<Props>(), {
  label: '',
  to: '',
  icon: '',
  color: 'primary',
  variant: 'link',
  size: 'sm',
  loading: false,
  disabled: false
})
</script>

<template>
  <UButton
    :to="to"
    :icon="icon"
    :color="color"
    :variant="variant"
    :size="size"
    :loading="loading"
    :disabled="disabled"
    class="px-5 py-2 text-sm font-medium border border-gray-300 dark:border-zinc-700 rounded-xl hover:bg-gray-100 dark:hover:bg-zinc-800 transition"
  >
    <template #default>
      <span v-if="label">
        {{ label }}
      </span>
      <slot v-else />
    </template>
  </UButton>
</template>
