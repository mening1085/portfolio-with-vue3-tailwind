<script setup>
import { Icon } from "@iconify/vue";
import Card from "./card/Card.vue";
import CardItem from "./card/CardItem.vue";
</script>
<template>
  <Card>
    <h1 class="mb-3 text-2xl font-semibold text-gray-600 dark:text-white">
      Information
    </h1>
    <CardItem
      class="mb-3"
      item-key="ปัจจุบันทำงานที่"
      item-value="KISRA"
      icon="fluent-mdl2:work"
      link="https://www.kisracorp.com/"
    />
    <CardItem
      class="mb-3"
      item-key="เคยฝึกงานที่"
      item-value="TARAD.com"
      icon="fluent-mdl2:work"
      link="https://www.tarad.com/"
    />
    <CardItem
      class="mb-3"
      item-key="เคยศึกษา คณะวิทยาศาสตร์ สาขาเทคโนโลยีสารสนเทศ"
      item-value="มหาวิทยาลัยนเรศวร"
      icon="mdi:education-outline"
      link="https://www.facebook.com/nu.university"
    />
    <CardItem
      class="mb-3"
      item-key="อาศัยอยู่ที่"
      item-value="กรุงเทพมหานคร"
      icon="ic:outline-home"
      link=""
    />

    <hr />
    <div class="flex justify-center mt-3">
      <a href="https://github.com/mening1085" target="_blank" class="mx-2">
        <Icon
          icon="mdi:github"
          class="text-4xl text-gray-600 dark:text-white hover:text-blue-500 dark:hover:text-gray-300 cursor-pointer"
        />
      </a>
      <a href="https://www.facebook.com/x.mmeenn" target="_blank" class="mx-2">
        <Icon
          icon="ic:baseline-facebook"
          class="text-4xl text-gray-600 dark:text-white hover:text-blue-500 dark:hover:text-gray-300 cursor-pointer"
        />
      </a>
      <a href="https://www.instagram.com/x.mmeenn" target="_blank" class="mx-2">
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
  </Card>
</template>

<style></style>
