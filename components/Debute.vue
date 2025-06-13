<template>
  <div
    class="absolute inset-0 flex flex-col items-center justify-center text-slate-200 font-mono text-base leading-relaxed z-10 pointer-events-none tracking-wide"
  >
    <div class="opacity-0 animate-fadein" :style="{ animationDelay: '300ms' }">
      系統提示
    </div>
    <div class="opacity-0 animate-fadein text-slate-300" :style="{ animationDelay: '1300ms' }">
      世界線已校準
    </div>
    <div class="opacity-0 animate-fadein text-slate-400" :style="{ animationDelay: '2300ms' }">
      六月，從線上走進現實
    </div>
  </div>
</template>

<style scoped>
@keyframes fadein {
  0% {
    opacity: 0;
    transform: translateY(0.75rem);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
.animate-fadein {
  animation: fadein 0.8s ease-out forwards;
}
</style>
