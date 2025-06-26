<script setup lang="ts">
import Badge from "./Badge.vue";
defineProps<{ status: "running" | "paused" }>();
// Using `defineModel` causes the type to be correctly inferred (defineEmits also works)
defineModel<boolean>();
</script>
<template>
  <Badge v-if="status == 'running'">{{ status }}</Badge>
  <Badge v-else-if="status == 'paused'">{{ status }}</Badge>
  <Badge v-else>{{ status }}</Badge>
</template>
