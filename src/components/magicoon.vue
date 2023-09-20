<script setup lang="ts">
import { computed, defineAsyncComponent } from "vue";

const props = defineProps({
  name: {
    type: String,
    required: true,
  },
  size: {
    type: [String, Number],
    default: 24,
  },
  type: {
    type: String,
    default: "Regular",
  },
  color: {
    type: String,
    default: "#000",
  },
});
const icon = computed(() => {
  return defineAsyncComponent(() => import(`./icons/${props.name}.vue`));
});
</script>

<template>
  <component :is="icon" :type="type" :color="color" :size="size" />
</template>
