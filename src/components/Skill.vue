<script setup>
import { onMounted, reactive, ref } from "vue";
import vueImage from "../assets/images/skill/vue.png";
import nuxtImage from "../assets/images/skill/nuxt.png";
import reactImage from "../assets/images/skill/react.png";
import laravelImage from "../assets/images/skill/laravel.png";
import phpImage from "../assets/images/skill/php.png";
import tailwindImage from "../assets/images/skill/tailwind.png";
import javascriptImage from "../assets/images/skill/js.png";
import mysqlImage from "../assets/images/skill/mysql.png";
import postgresqlImage from "../assets/images/skill/postgreSQL.png";
import nodeImage from "../assets/images/skill/node.png";

const images = reactive([
  {
    src: vueImage,
  },
  {
    src: nuxtImage,
  },
  {
    src: reactImage,
  },
  {
    src: laravelImage,
  },
  {
    src: phpImage,
  },
  {
    src: tailwindImage,
  },
  {
    src: javascriptImage,
  },
  {
    src: mysqlImage,
  },
  {
    src: postgresqlImage,
  },
  {
    src: nodeImage,
  },
]);
</script>

<template>
  <div class="grid grid-cols-5 gap-4">
    <div class="p-6 flex justify-center" v-for="(item, i) in images" :key="i">
      <img
        @click="toggleDialog(item.src)"
        class="object-center object-contain w-full rounded h-48 overflow-hidden"
        :src="item.src"
      />
    </div>
  </div>
</template>

<style></style>
