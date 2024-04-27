<script>
import ImgCar from "../../json/cars.json";
import "./Gallery.css";
export default {
  data() {
    return {
      images: ImgCar,
    };
  },
  methods: {
    getImageUrl(name) {
      return new URL(`../../assets/imgs/Gallery/${name}.jpg`, import.meta.url)
        .href;
    },
  },
};
</script>

<template>
  <div class="gallery bg-gray-200 dark:bg-blue-950 pt-6 pb-20" id="gallery">
    <h2 class="main-title">المعرض</h2>
    <div class="container grid grid-cols-3 gap-4">
      <div
        class="box p-2 border-2 border-red-700 bg-white dark:bg-gray-800 max-h-90 rounded-md shadow-md shadow-blue-400/30 hover:shadow-blue-300/60"
        v-for="image in images"
        :key="image.id"
      >
        <div class="image">
          <img :src="getImageUrl(image.img)" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>
