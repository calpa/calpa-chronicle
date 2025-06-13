<template>
  <Card>
    <!-- 標題 -->
    <div
      class="flex items-center justify-center gap-3 text-2xl font-extrabold tracking-wider"
    >
      <span v-if="filter === 'before'">精彩回顧 🔥</span>
    </div>

    <!-- 活動列表 -->
    <div>
      <div
        v-for="(event, index) in filteredEvents"
        :key="index"
        :style="{ animationDelay: `${index * 300 + 300}ms` }"
      >
        <div
          class="flex flex-row items-center mb-2"
          :class="[getEventColor(event.date)]"
        >
          <div class="text-sm">{{ event.icon }}</div>
          <div class="font-semibold text-base flex-1">{{ event.title }}</div>
          <div v-if="event.desc" class="text-sm bg-white/10 px-2 py-1 mt-1">
            {{ event.desc }}
          </div>
          <div class="text-xs mt-1">{{ event.date }}</div>
        </div>
      </div>
    </div>

    <div class="text-xl font-bold text-center text-green-600">
      超過 700 人參加！
    </div>
  </Card>
</template>

<script setup lang="ts">
import { computed } from "vue";
import dayjs from "dayjs";

import events from "../constants/events";

const props = defineProps({
  filter: {
    type: String,
    default: "all",
  },
  eventDate: {
    type: String,
    default: "2025-05-24",
  },
});

const filteredEvents = computed(() => {
  let result = events;

  if (props.filter === "all") {
    return events;
  } else if (props.filter === "before") {
    result = events.filter((event) => {
      return (
        dayjs(event.date).isBefore(dayjs(props.eventDate)) ||
        dayjs(event.date).isSame(dayjs(props.eventDate))
      );
    });
  } else if (props.filter === "after") {
    result = events.filter((event) => {
      return dayjs(event.date).isAfter(dayjs(props.eventDate));
    });
  }

  result.sort((a, b) => {
    return dayjs(a.date).isBefore(dayjs(b.date)) ? 1 : -1;
  });

  return result;
});

const getEventColor = (date: string) => {
  const eventDate = dayjs(date);
  const today = dayjs(props.eventDate);
  if (eventDate.isBefore(today)) {
    return "text-slate-300";
  } else if (eventDate.isSame(today)) {
    return "text-yellow-300";
  } else {
    return "text-blue-300";
  }
};
</script>
