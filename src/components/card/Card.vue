<template>
  <div
    :class="
      'p-4 rounded-lg border border-black dark:border-gray-500 shadow-2xl shadow-[7px_7px_0px_0px_rgba(0,0,0)] dark:shadow-white/20 bg-white dark:bg-gray-900 dark:text-white' +
      ' ' +
      customClass
    "
  >
    <slot />
  </div>
</template>

<script>
export default {
  props: {
    customClass: {
      type: String,
      default: "",
    },
    customStyle: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="scss"></style>
