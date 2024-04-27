<template>
  <div class="discount flex" id="discount">
    <div class="image text-white flex items-center justify-center relative">
      <div class="content text-center">
        <h2 class="text-4xl mb-4">اسعارنا مناسبة للجيع</h2>
        <p class="leading-9 text-xl w-4/5 m-auto">
          لدينا اسعار بسيطة وفي متناول اليد وايضا تجربة تنقلك الي عالم اخر
          وستشعر معنا بالتميز و الاختلاف بأذن الله
        </p>
        <img src="../../assets/imgs/discount.png" class="w-72 m-auto" alt="" />
      </div>
    </div>
    <div class="form dark:bg-gray-900 flex items-center justify-center pb-9">
      <div class="content">
        <h2 class="dark:text-white text-4xl text-center mb-7">تواصل معنا</h2>
        <form action="">
          <input
            class="input w-96 p-2 mb-4 border-b-2 border-red-700 bg-gray-100 dark:bg-gray-800 dark:text-white"
            type="text"
            placeholder="أسمك"
            name="name"
          />
          <input
            class="input w-96 p-2 mb-4 border-b-2 border-red-700 bg-gray-100 dark:bg-gray-800 dark:text-white"
            type="email"
            placeholder="الأميل"
            name="email"
          />
          <input
            class="input w-96 p-2 mb-4 border-b-2 border-red-700 bg-gray-100 dark:bg-gray-800 dark:text-white"
            type="text"
            placeholder="رقم التليفون"
            name="mobile"
          />
          <textarea
            class="input w-96 p-2 mb-4 border-b-2 border-red-700 bg-gray-100 dark:bg-gray-800 dark:text-white"
            placeholder="أخبرنا ما الذي تحتاحه"
            name="message"
          ></textarea>
          <input type="submit" value="إرسال" />
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import "./Discount.css";
export default {};
</script>
