<template>
  <CardList 
    :items="filteredEvents"
    title="精彩回顧 🔥"
    footer="超過 1000 人參加！"
  />
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
