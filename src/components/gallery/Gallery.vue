<script setup>
import { ref, watch, reactive } from "vue";
import { Icon } from "@iconify/vue";
import image1 from "../../assets/images/gallery/me.jpeg";
import image2 from "../../assets/images/gallery/me_1.png";
import image3 from "../../assets/images/gallery/me_2.jpeg";
import image4 from "../../assets/images/gallery/me_4.jpeg";
import image5 from "../../assets/images/gallery/me_5.jpeg";
import image6 from "../../assets/images/gallery/me_8.jpeg";

const isDialog = ref(false);
const images = reactive([
  { src: image1 },
  { src: image2 },
  { src: image3 },
  { src: image4 },
  { src: image5 },
  { src: image6 },
]);

const imgSrc = ref("");
const toggleDialog = (image) => {
  imgSrc.value = image;
  isDialog.value = !isDialog.value;
};
</script>
<template>
  <div>
    <div class="grid grid-cols-3 gap-4">
      <div
        class="bg-gray-100 dark:bg-gray-800 rounded-md shadow-md"
        v-for="(item, i) in images"
        :key="i"
      >
        <img
          @click="toggleDialog(item.src)"
          class="object-center object-cover w-full rounded h-48 overflow-hidden"
          :src="item.src"
          alt="banner"
        />
      </div>
    </div>

    <div
      v-if="isDialog"
      @click="toggleDialog()"
      class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center"
    >
      <div class="bg-white rounded-md shadow-md relative">
        <button
          @click="toggleDialog()"
          class="w-6 h-6 flex justify-center items-center bg-gray-900 rounded-full shadow-md absolute top-2 right-2 z-20"
        >
          <Icon icon="fa-solid:times" class="text-sm text-white" />
        </button>
        <img
          class="object-center object-cover overflow-hidden max-w-3xl max-h-3xl"
          :src="imgSrc"
          alt="banner"
        />
      </div>
    </div>
  </div>
</template>

<style></style>
