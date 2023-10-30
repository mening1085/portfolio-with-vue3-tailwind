<script setup>
import TabItem from "../tabs/TabItem.vue";
defineProps({
  tabs: Number,
});
</script>
<template>
  <div
    class="text-sm font-medium text-center text-gray-700 border-b border-gray-200 dark:text-gray-500 dark:border-gray-700"
  >
    <ul class="flex flex-wrap -mb-px">
      <tab-item
        :value="tabs"
        :tabs="0"
        title="Experience"
        @onClickItemTab="$emit('onClickTab', $event)"
      />
      <tab-item
        :value="tabs"
        :tabs="1"
        title="Skill"
        @onClickItemTab="$emit('onClickTab', $event)"
      />
      <!-- <tab-item
        :value="tabs"
        :tabs="2"
        title="Hobbies"
        @onClickItemTab="$emit('onClickTab', $event)"
      />
      <tab-item
        :value="tabs"
        :tabs="3"
        title="Contacts"
        @onClickItemTab="$emit('onClickTab', $event)"
      /> -->
    </ul>
  </div>
</template>

<style></style>
