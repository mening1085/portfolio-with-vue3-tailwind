<script setup>
import { Icon } from "@iconify/vue";
defineProps({
  icon: String,
  itemKey: String,
  itemValue: String,
  link: String,
});
</script>

<template>
  <div class="flex items-center">
    <div class="shrink">
      <Icon :icon="icon" class="text-3xl" />
    </div>
    <div class="pl-2 dark:text-gray-400">
      {{ itemKey }}
      <a
        v-if="link"
        :href="link"
        target="_blank"
        class="font-medium hover:text-blue-500 dark:text-blue-500"
      >
        {{ itemValue }}
      </a>
      <span v-else class="font-medium">{{ itemValue }}</span>
    </div>
  </div>
</template>

<style></style>
