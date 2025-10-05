<template>
  <div class="qr-code-container" :class="containerClass">
    <div class="qr-code-wrapper">
      <QrcodeVue
        :value="value"
        :size="size"
        :level="level"
        :render-as="renderAs"
        :background="background"
        :foreground="foreground"
        :margin="margin"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import QrcodeVue from 'qrcode.vue'

interface Props {
  value: string
  size?: number
  level?: 'L' | 'M' | 'Q' | 'H'
  renderAs?: 'canvas' | 'svg'
  background?: string
  foreground?: string
  margin?: number
  rounded?: boolean
  shadow?: boolean
  padding?: number
  class?: string
}

const props = withDefaults(defineProps<Props>(), {
  size: 256,
  level: 'H',
  renderAs: 'canvas',
  background: '#ffffff',
  foreground: '#000000',
  margin: 2,
  rounded: true,
  shadow: true,
  padding: 16,
  class: ''
})

const containerClass = computed(() => {
  const classes = [props.class]
  if (props.rounded) classes.push('rounded-2xl')
  if (props.shadow) classes.push('shadow-lg')
  return classes.filter(Boolean).join(' ')
})
</script>

<style scoped>
.qr-code-container {
  display: inline-block;
  background: white;
  padding: v-bind('props.padding + "px"');
  line-height: 0;
}

.qr-code-wrapper {
  line-height: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.qr-code-wrapper canvas,
.qr-code-wrapper svg {
  display: block;
  border-radius: 8px;
}
</style>
