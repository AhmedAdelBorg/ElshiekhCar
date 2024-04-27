<script>
import { useDark } from "@vueuse/core";
const isDark = useDark();
import LandingVue from "@/components/Home/Landing.vue";
import BrandsCar from "@/components/Home/BrandsCar.vue";
import GalleryVue from "@/components/Home/Gallery.vue";
import FeaturesVue from "@/components/Home/Features.vue";
import WorkStepsVue from "@/components/Home/WorkSteps.vue";
import ExhibitionsVue from "@/components/Home/Exhibitions.vue";
import ServicesVue from "@/components/Home/Services.vue";
import SkillsVue from "@/components/Home/Skills.vue";
import PricingVue from "@/components/Home/Pricing.vue";
import videosVue from "@/components/Home/videos.vue";
import StatsVue from "@/components/Home/Stats.vue";
import DiscountVue from "@/components/Home/Discount.vue";
import FooterVue from "@/components/Home/Footer.vue";
export default {
  name: "HomeView",
  data() {
    return {
      dark: isDark,
    };
  },
  components: {
    LandingVue,
    BrandsCar,
    GalleryVue,
    FeaturesVue,
    WorkStepsVue,
    ExhibitionsVue,
    ServicesVue,
    SkillsVue,
    PricingVue,
    videosVue,
    StatsVue,
    DiscountVue,
    FooterVue,
  },
};
</script>

<template>
  <landing-vue />
  <brands-car />
  <div class="spikes relative" v-if="!dark"></div>
  <gallery-vue />
  <features-vue />
  <work-steps-vue />
  <exhibitions-vue />
  <div class="spikes relative" v-if="!dark"></div>
  <services-vue />
  <skills-vue />
  <pricing-vue />
  <videos-vue />
  <stats-vue />
  <discount-vue />
  <footer-vue />
</template>
