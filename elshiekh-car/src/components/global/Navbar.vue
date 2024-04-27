<script setup>
import { useDark, useToggle } from "@vueuse/core";
const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <nav class="dark:bg-blue-950">
    <div
      class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-3"
    >
      <router-link to="/">
        <a href="/" class="flex items-center space-x-3 rtl:space-x-reverse">
          <img src="/logo.png" class="h-10" alt="ELSHIEKH-CAR Logo" />
          <span
            class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white"
            >الشيخ كــار</span
          >
        </a>
      </router-link>
      <button
        data-collapse-toggle="navbar-default"
        type="button"
        class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-white dark:hover:bg-blue-900 dark:focus:ring-blue-900"
        aria-controls="navbar-default"
        aria-expanded="false"
      >
        <span class="sr-only">Open main menu</span>
        <svg
          class="w-5 h-5"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 17 14"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M1 1h15M1 7h15M1 13h15"
          />
        </svg>
      </button>
      <div class="w-full md:block md:w-auto" id="navbar-default">
        <ul
          class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg md:flex-row md:space-x-10 rtl:space-x-reverse md:mt-0 md:border-0 dark:border-blue-700"
        >
          <router-link to="/">
            <li>
              <a
                class="block py-2 px-3 dark:text-white rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-red-500 md:p-0"
                aria-current="page"
              >
                الرئيسية</a
              >
            </li>
          </router-link>

          <router-link to="/buy">
            <li>
              <a
                class="block py-2 px-3 dark:text-white rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-red-500 md:p-0"
                aria-current="page"
                >شراء</a
              >
            </li>
          </router-link>

          <li>
            <a
              href="#"
              class="block py-2 px-3 dark:text-white rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-red-500 md:p-0"
              >بيع</a
            >
          </li>
          <li>
            <a
              href="#"
              class="block py-2 px-3 dark:text-white rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-red-500 md:p-0"
              >تأجير</a
            >
          </li>
          <li>
            <a
              href="#"
              class="block py-2 px-3 dark:text-white rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-red-500 md:p-0"
            >
              <div>
                <span class="icon-language"></span>
              </div>
            </a>
          </li>
          <li>
            <a
              href="#"
              class="block py-2 px-3 dark:text-white rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-red-500 md:p-0"
              ><span class="icon-moon" @click="toggleDark()"></span
            ></a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style>
@media (width < 768px) {
  .visible {
    display: none;
  }
}
</style>
