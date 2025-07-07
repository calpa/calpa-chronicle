<template>
  <div
    class="flex justify-between absolute bottom-0 w-full p-1 z-10"
    v-if="$nav.currentPage !== 1"
  >
    <div class="text-xs text-white/40">
      ことばと式で、あたらしい現実を錬成する。
    </div>
    <div class="text-xs text-white/40 text-right">
      {{
        $slidev.configs.footerRightText ||
        "© Calpa 的煉金工房. All rights reserved."
      }}
    </div>
  </div>
</template>
