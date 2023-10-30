<script setup>
import VueWriter from "vue-writer";
</script>

<template>
  <div
    class="bg-white dark:bg-gray-900 shadow-lg shadow-black/5 dark:shadow-white/10 border-b pb-4"
  >
    <div class="containerr mx-auto">
      <!-- header -->
      <div>
        <img
          class="object-center object-cover w-full rounded-b max-h-80 overflow-hidden"
          src="../assets/images/banner.webp"
          alt="banner"
        />
      </div>

      <div class="container mx-auto px-0 sm:px-6">
        <div class="grid md:grid-flow-col md:auto-cols-max gap-4">
          <div class="flex justify-center">
            <img
              class="w-52 h-52 rounded-full object-cover object-top overflow-hidden -mt-24 border-8 border-white dark:shadow-md dark:shadow-white/60"
              src="../assets/images/gallery/me_8.jpeg"
              alt="avatar"
            />
          </div>
          <div class="text-center sm:text-left pt-0 sm:pt-2">
            <div class="">
              <div>
                <div class="text-5xl font-bold dark:text-white border-b pb-1">
                  <VueWriter
                    :typeSpeed="100"
                    :delay="10000"
                    :array="['Kasem Tanson']"
                  />
                </div>
                <div
                  class="text-xl mt-1 font-semibold text-gray-600 dark:text-gray-400"
                >
                  <VueWriter
                    :typeSpeed="40"
                    :delay="10000"
                    :start="1000"
                    :array="['Full-Stack Developer / Photographer']"
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
      </div>

      <!-- end header -->
    </div>
  </div>
</template>

<style></style>
