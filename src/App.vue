<template>
  <MainNavbar />
  <section id="home"><MainBanner /></section>
  <section id="about"><AboutUs /></section>
  <section id="statistics"><FunFacts /></section>
  <section id="programs"><PopularCourses /></section>
  <section id="testimonials"><TestimonialContent /></section>
  <section id="contact"><ContactUs /></section>
  <MainFooter />
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import MainNavbar from "./components/Layouts/MainNavbar.vue";
import MainBanner from "./components/HomeOne/MainBanner.vue";
import AboutUs from "./components/HomeOne/AboutUs.vue";
import PopularCourses from "./components/HomeOne/PopularCourses.vue";
import TestimonialContent from "./components/HomeOne/TestimonialContent.vue";
import FunFacts from "./components/HomeOne/FunFacts.vue";
import ContactUs from "./components/Contact/ContactUs.vue";
import MainFooter from "./components/Layouts/MainFooter.vue";

export default defineComponent({
  name: "App",
  components: {
    MainNavbar,
    MainBanner,
    AboutUs,
    PopularCourses,
    TestimonialContent,
    FunFacts,
    ContactUs,
    MainFooter,
  },
  setup() {
    const isLoading = ref(false); // PreLoader removed for simplicity
    return {
      isLoading,
    };
  },
});
</script>

<style scoped>
.statistics-section {
  padding: 100px 0;
  background-color: #f8f9fa;
}

.statistics-content h2 {
  color: var(--mainColor);
  margin-bottom: 40px;
}

.stat-card {
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 2px 12px rgba(0,0,0,0.06);
  padding: 32px 16px;
  margin: 0 auto;
}

.stat-card h3 {
  color: var(--mainColor);
  font-size: 2.5rem;
  margin-bottom: 12px;
}

.stat-card p {
  color: var(--paragraphColor);
  font-size: 1.1rem;
  margin-bottom: 0;
}
</style>