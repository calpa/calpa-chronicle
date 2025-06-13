<template>
  <div
    class="w-full mx-auto bg-gradient-to-br from-[#223061] to-[#191f36] shadow-2xl flex flex-col gap-4 text-white relative border border-slate-600"
    :class="paddingClass"
  >
    <div
      class="border border-slate-600 w-[calc(100%-1rem)] h-[calc(100%-1rem)] absolute top-2 left-2"
    />
    <slot />
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps({
  padding: {
    type: String,
    default: '16', // options: '8' or '16'
  },
})

const paddingClass = computed(() =>
  props.padding === '8' ? 'p-8' : 'p-16'
)
</script>