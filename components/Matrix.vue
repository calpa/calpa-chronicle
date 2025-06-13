<!-- MatrixRain.vue -->
<template>
  <div class="absolute inset-0 overflow-hidden z-0">
    <canvas ref="canvas" class="w-full h-full" v-click></canvas>
    <Debut v-click />
  </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue'

const canvas = ref<HTMLCanvasElement | null>(null)

onMounted(() => {
  const c = canvas.value!
  const ctx = c.getContext('2d')!
  c.width = window.innerWidth
  c.height = window.innerHeight

  const katakana = 'アカサタナハマヤラワ0123456789'.split('')
  const fontSize = 14
  const columns = c.width / fontSize
  const drops = Array.from({ length: columns }, () => 1)

  function draw() {
    ctx.fillStyle = 'rgba(0, 0, 0, 0.05)'
    ctx.fillRect(0, 0, c.width, c.height)
    ctx.fillStyle = '#0f0'
    ctx.font = `${fontSize}px monospace`

    for (let i = 0; i < drops.length; i++) {
      const text = katakana[Math.floor(Math.random() * katakana.length)]
      ctx.fillText(text, i * fontSize, drops[i] * fontSize)

      if (drops[i] * fontSize > c.height && Math.random() > 0.975) {
        drops[i] = 0
      }

      drops[i]++
    }
  }

  setInterval(draw, 40)
})
</script>
