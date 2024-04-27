<script>
import BrandsCar from "../../json/brands.json";
export default {
  name: "BrandsCar",
  data() {
    return {
      brands: BrandsCar,
    };
  },
  methods: {
    getImageUrl(name) {
      return new URL(`../../assets/imgs/Brands/${name}.png`, import.meta.url)
        .href;
    },
  },
};
</script>

<template>
  <div class="brands relative bg-white dark:bg-blue-950 pt-9 pb-20" id="brands">
    <h1 class="main-title">الماركات</h1>
    <div class="container grid grid-cols-6 gap-9">
      <div
        class="box bg-white dark:bg-gray-800 text-center max-h-90 rounded-md shadow-md shadow-gray-400/30 hover:shadow-gray-300/60"
        v-for="brand in brands"
        :key="brand.id"
      >
        <img class="max-w-24 m-auto" :src="getImageUrl(brand.img)" alt="" />
        <div class="content p-2 mb-2 dark:text-white">
          <h2>{{ brand.title }}</h2>
        </div>
        <div
          class="info p-3 flex items-center justify-between md:text-red-500 font-bold border-t border-gray-300 dark:border-gray-700"
        >
          <a href="">المزيد</a>
          <span class="icon icon-long-arrow-left"></span>
        </div>
      </div>
    </div>
  </div>
</template>
