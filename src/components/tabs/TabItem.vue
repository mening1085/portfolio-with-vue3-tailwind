<script setup>
defineProps({
  tabs: Number,
  value: Number,
  title: String,
});
</script>

<template>
  <li>
    <a
      :class="{
        'border-b-2 text-blue-500 border-blue-500 dark:border-blue-500 dark:text-blue-500':
          tabs == value,
      }"
      class="inline-block p-4 hover:border-b-2 hover:border-blue-500 hover:text-blue-500 rounded-t-lg dark:border-blue-500 cursor-pointer dark:hover:border-blue-500 dark:hover:text-blue-500"
      @click="$emit('onClickItemTab', tabs)"
    >
      {{ title }}
    </a>
  </li>
</template>

<style></style>
