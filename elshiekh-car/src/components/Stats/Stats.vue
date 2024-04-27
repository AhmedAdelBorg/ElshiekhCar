<template>
  <div
    class="stats relative min-h-60 pt-24 pb-24 before:bg-gray-100 before:bg-opacity-90 dark:before:bg-blue-950 dark:before:bg-opacity-90"
    id="stats"
  >
    <h2 class="main-title">احصائيات الموقع</h2>
    <div class="container grid grid-cols-4 gap-4">
      <div class="box relative bg-white dark:bg-gray-900 text-center py-6">
        <span class="text-5xl dark:text-white icon-group"></span>
        <span class="number block text-5xl dark:text-white my-4" data-goal="150"
          >150</span
        >
        <span class="text-red-600 font-bold text-2xl">العملاء</span>
      </div>
      <div class="box relative bg-white dark:bg-gray-900 text-center py-6">
        <span class="text-5xl dark:text-white icon-money"></span>
        <span class="number block text-5xl dark:text-white my-4" data-goal="135"
          >135</span
        >
        <span class="text-red-600 font-bold text-2xl">البيع</span>
      </div>
      <div class="box relative bg-white dark:bg-gray-900 text-center py-6">
        <span class="text-5xl dark:text-white icon-bitcoin"></span>
        <span class="number block text-5xl dark:text-white my-4" data-goal="50"
          >50</span
        >
        <span class="text-red-600 font-bold text-2xl">الشراء</span>
      </div>
      <div class="box relative bg-white dark:bg-gray-900 text-center py-6">
        <span class="text-5xl dark:text-white icon-credit-card"></span>
        <span class="number block text-5xl dark:text-white my-4" data-goal="300"
          >300</span
        >
        <span class="text-red-600 font-bold text-2xl">التأجير</span>
      </div>
    </div>
  </div>
</template>

<script>
import "./Stats.css";
export default {};
</script>
