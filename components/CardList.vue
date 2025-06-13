<template>
  <Card>
    <div
      class="flex items-center justify-center gap-3 text-2xl font-extrabold tracking-wider"
      v-if="title"
    >
      {{ title }}
    </div>

    <div v-if="items.length > 0">
      <div
        v-for="(item, index) in items"
        :key="index"
        :class="item.className"
        class="flex flex-row items-center mb-2 px-2"
      >
        <div class="text-sm">{{ item.icon }}</div>
        <div class="font-semibold text-base flex-1">{{ item.title }}</div>
        <div v-if="item.desc" class="text-sm bg-white/10 px-2 py-1 mt-1 mr-2">
          {{ item.desc }}
        </div>
        <div class="text-xs mt-1">{{ item.date }}</div>
      </div>
    </div>

    <div class="text-xl font-bold text-center text-green-600" v-if="footer">
      {{ footer }}
    </div>
  </Card>
</template>

<script setup lang="ts">
type Item = {
  icon: string;
  title: string;
  desc?: string;
  date: string;
  className?: string;
};

const props = defineProps({
  items: {
    type: Array<Item>,
    default: () => [],
  },
  title: {
    type: String,
    default: "",
  },
  footer: {
    type: String,
    default: "",
  },
});
</script>
