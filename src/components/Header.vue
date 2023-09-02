<script setup>
import VueWriter from "vue-writer";
</script>

<template>
  <div
    class="bg-white dark:bg-gray-900 shadow-lg shadow-black/5 dark:shadow-white/10 border-b pb-4"
  >
    <div class="container mx-auto">
      <!-- header -->
      <div class="-mx-8">
        <img
          class="object-center object-cover w-full rounded-b max-h-80 overflow-hidden"
          src="../assets/images/banner.webp"
          alt="banner"
        />
      </div>

      <div class="flex">
        <div class="shrink">
          <img
            class="w-52 h-52 rounded-full object-cover overflow-hidden -mt-24 border-8 border-white dark:shadow-md dark:shadow-white/60"
            src="../assets/images/avatar.JPG"
            alt="avatar"
          />
        </div>
        <div class="flex-1 pl-4 pt-2">
          <div class="flex justify-between items-center">
            <div>
              <div class="text-5xl font-bold dark:text-white border-b pb-1">
                <VueWriter
                  :typeSpeed="100"
                  :delay="100000"
                  :array="['Kasem Tanson']"
                />
              </div>
              <div
                class="text-2xl mt-1 font-semibold text-gray-600 dark:text-gray-400"
              >
                <VueWriter
                  :typeSpeed="100"
                  :delay="100000"
                  :start="1500"
                  :array="['Web Developer / Photographer']"
                />
              </div>
            </div>
            <!-- <div>
              <button
                class="px-4 py-2 text-white bg-gray-600 dark:bg-blue-500 rounded-md"
              >
                Download CV
              </button>
            </div> -->
          </div>
        </div>
      </div>
      <!-- end header -->
    </div>
  </div>
</template>

<style></style>
