<script setup>
import { onMounted, ref, watch } from "vue";
import { Icon } from "@iconify/vue";

import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Card from "./components/card/Card.vue";
import Information from "./components/Information.vue";
import Tab from "./components/tabs/Tab.vue";
import Gallery from "./components/gallery/Gallery.vue";
import Skill from "./components/Skill.vue";
import Portfolio from "./components/Portfolio.vue";
import Hobby from "./components/Hobby.vue";

const isDark = ref(false);
const showInfo = ref(false);
const showHeader = ref(false);
const showGallery = ref(false);
const showContent = ref(false);
const showFooter = ref(false);
const tabs = ref(0);

const toggleDark = () => {
  isDark.value = !isDark.value;
};

const changeTab = (tab) => {
  tabs.value = tab;
};

watch(isDark, async (newQuestion, oldQuestion) => {
  if (newQuestion) {
    document.documentElement.classList.add("dark");
  } else {
    document.documentElement.classList.remove("dark");
  }
});

onMounted(() => {
  setTimeout(() => {
    showHeader.value = true;
  }, 100);
  setTimeout(() => {
    showInfo.value = true;
  }, 1000);
  setTimeout(() => {
    showGallery.value = true;
  }, 1500);
  setTimeout(() => {
    showContent.value = true;
  }, 2000);
  setTimeout(() => {
    showFooter.value = true;
  }, 2500);
});
</script>

<template>
  <div class="bg-gray-100 dark:bg-gray-800 h-screen">
    <button
      @click="toggleDark()"
      class="px-4 py-2 text-white fixed top-4 right-4 rounded-md"
    >
      <Icon
        :icon="isDark ? 'fa-solid:sun' : 'fa-solid:moon'"
        class="text-2xl text-gray-600 dark:text-white hover:text-gray-400 dark:hover:text-gray-300"
      />
    </button>

    <!-- Header -->
    <Transition
      name="custom-classes"
      enter-active-class="animate__animated animate__fadeInDown"
    >
      <Header v-if="showHeader" />
    </Transition>

    <div class="pt-6 pb-12 bg-gray-100 dark:bg-gray-800 px-0 sm:px-6">
      <div class="container mx-auto">
        <div class="flex gap-4 flex-col lg:flex-row">
          <!-- Information -->
          <div class="md:basis-1/3 basis-full">
            <!-- Information -->
            <Transition name="slide-fade" mode="out-in">
              <Information v-if="showInfo" />
            </Transition>

            <Transition name="slide-fade">
              <Card class="mt-6" v-if="showGallery">
                <gallery />
              </Card>
            </Transition>
          </div>

          <!-- Tab -->
          <div class="md:basis-2/3 basis-full">
            <Transition name="slide-fade">
              <Card v-if="showContent">
                <!-- Tab -->
                <Tab :tabs="tabs" @onClickTab="changeTab($event)" />

                <!-- Tab content -->
                <Transition name="slide-fade">
                  <div v-if="tabs == 0">
                    <Portfolio />
                  </div>
                </Transition>
                <Transition name="slide-fade">
                  <div v-if="tabs == 1">
                    <Skill />
                  </div>
                </Transition>
                <Transition name="slide-fade">
                  <div v-if="tabs == 2">
                    <hobby />
                  </div>
                </Transition>
                <Transition name="slide-fade">
                  <div v-if="tabs == 3">
                    <div class="mt-6">
                      <h1 class="text-2xl font-bold">Contact</h1>
                      <p class="mt-2">Lorem ipsum</p>
                    </div>
                  </div>
                </Transition>
              </Card>
            </Transition>
          </div>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <Transition
      name="custom-classes"
      enter-active-class="animate__animated animate__fadeInDown"
    >
      <Footer v-if="showFooter" />
    </Transition>
  </div>
</template>

<style scoped lang="scss">
.slide-fade-enter-active {
  transition: all 0.5s ease-out;
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}
</style>
