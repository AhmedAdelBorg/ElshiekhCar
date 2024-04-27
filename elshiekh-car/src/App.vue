<script>
import Navbar from "./components/global/Navbar.vue";

export default {
  data() {
    return {
      active: "",
    };
  },

  components: {
    Navbar,
  },

  methods: {},

  mounted() {
    document.addEventListener("scroll", () => {
      window.scrollY >= 800 ? (this.active = "active") : (this.active = "");
    });
  },
};
</script>

<template>
  <Navbar />
  <router-view />
  <a
    href="#"
    :class="active"
    class="fixed bg-white border-2 border-red-700 rounded-full bg-blue-950 dark:bg-gray-800 dark:text-white flex items-center justify-center"
  >
    <span className="icon-keyboard_arrow_up "></span>
  </a>
</template>

<style scoped>
a {
  width: 2.6rem;
  height: 2.6rem;
  bottom: 2rem;
  right: 3%;
  text-align: center;
  font-size: 2rem;
  visibility: hidden;
  opacity: 0;
  z-index: 999;
}
.active {
  visibility: visible;
  opacity: 1;
}
</style>
