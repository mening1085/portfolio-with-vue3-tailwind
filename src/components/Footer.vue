<script setup>
import { Icon } from "@iconify/vue";
</script>
<template>
  <div class="border-t-2 py-4 border-gray-200 dark:bg-gray-800">
    <div
      class="container mx-auto flex justify-center sm:justify-between items-center flex-wrap"
    >
      <div class="flex justify-center mb-4 sm:mb-0">
        <a href="https://github.com/mening1085" target="_blank" class="mx-2">
          <Icon
            icon="mdi:github"
            class="text-4xl text-gray-600 dark:text-white hover:text-blue-500 dark:hover:text-gray-300 cursor-pointer"
          />
        </a>
        <a
          href="https://www.facebook.com/x.mmeenn"
          target="_blank"
          class="mx-2"
        >
          <Icon
            icon="ic:baseline-facebook"
            class="text-4xl text-gray-600 dark:text-white hover:text-blue-500 dark:hover:text-gray-300 cursor-pointer"
          />
        </a>
        <a
          href="https://www.instagram.com/x.mmeenn"
          target="_blank"
          class="mx-2"
        >
          <Icon
            icon="ri:instagram-fill"
            class="text-4xl text-gray-600 dark:text-white hover:text-blue-500 dark:hover:text-gray-300 cursor-pointer"
          />
        </a>
        <a
          href="https://www.linkedin.com/in/kasem-tanson-92b2b51a2/"
          target="_blank"
          class="mx-2"
        >
          <Icon
            icon="mdi:linkedin"
            class="text-4xl text-gray-600 dark:text-white hover:text-blue-500 dark:hover:text-gray-300 cursor-pointer"
          />
        </a>
      </div>
      <div class="flex justify-center items-center">
        <p class="text-gray-500 dark:text-gray-400 pr-4">
          © 2023 - All rights reserved
        </p>
      </div>
    </div>
  </div>
</template>

<style></style>
