<script>
import exhibitions from "../../json/exhibitions.json";
export default {
  data() {
    return {
      exhibitions: exhibitions,
    };
  },
  methods: {
    getImageUrl(name) {
      return new URL(`../../assets/imgs/${name}.jpg`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div
    class="exhibitions bg-white dark:bg-blue-950 pt-24 pb-20"
    id="exhibitions"
  >
    <h2 class="main-title">أهم المعارض</h2>
    <div class="container grid grid-cols-4 gap-6">
      <div
        class="box relative bg-gray-100 dark:bg-gray-800 rounded-lg"
        v-for="exhibition in exhibitions"
        :key="exhibition.id"
      >
        <div class="data flex items-center pt-9">
          <img :src="getImageUrl(exhibition.img)" alt="" class="rounded-lg" />
          <div class="social flex flex-col items-center gap-6">
            <a href="#" class="w-14 h-6 flex justify-center items-center">
              <span
                class="icon text-xl text-gray-500 hover:text-red-600 icon-facebook"
              ></span>
            </a>
            <a
              href="#"
              class="w-14 h-6 flex justify-center items-center hover:text-red-600"
            >
              <span
                class="icon text-xl text-gray-500 hover:text-red-600 icon-twitter1"
              ></span>
            </a>
            <a
              href="#"
              class="w-14 h-6 flex justify-center items-center hover:text-red-600"
            >
              <span
                class="icon text-xl text-gray-500 hover:text-red-600 icon-linkedin-square"
              ></span>
            </a>
            <a
              href="#"
              class="w-14 h-6 flex justify-center items-center hover:text-red-600"
            >
              <span
                class="icon text-xl text-gray-500 hover:text-red-600 icon-youtube-play"
              ></span>
            </a>
          </div>
        </div>
        <div class="info pr-6">
          <h3 class="text-2xl mt-3 dark:text-white">{{ exhibition.title }}</h3>
          <p class="my-4 text-gray-700 dark:text-gray-400">
            {{ exhibition.description }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
