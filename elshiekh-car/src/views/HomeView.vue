<script>
import { useDark } from "@vueuse/core";
const isDark = useDark();
import LandingVue from "@/components/Landing/Landing.vue";
import BrandsCar from "@/components/BrandsCar/BrandsCar.vue";
import GalleryVue from "@/components/Gallery/Gallery.vue";
import FeaturesVue from "@/components/Features/Features.vue";
import WorkStepsVue from "@/components/WorkSteps/WorkSteps.vue";
import ExhibitionsVue from "@/components/Exhibitions/Exhibitions.vue";
import ServicesVue from "@/components/Services/Services.vue";
import SkillsVue from "@/components/Skills/Skills.vue";
import PricingVue from "@/components/Pricing/Pricing.vue";
import videosVue from "@/components/videos/videos.vue";
import StatsVue from "@/components/Stats/Stats.vue";
import DiscountVue from "@/components/Discount/Discount.vue";
import FooterVue from "@/components/Footer/Footer.vue";
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
