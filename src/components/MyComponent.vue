<script setup lang="ts">
import Badge from "./Badge.vue";
defineProps<{ status: "running" | "paused" }>();
</script>
<template>
  <Badge v-if="status == 'running'">{{ status }}</Badge>
  <Badge v-else-if="status == 'paused'">{{ status }}</Badge>
  <Badge v-else>{{ status }}</Badge>
</template>
