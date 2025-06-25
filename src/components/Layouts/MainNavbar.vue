<template>
  <div :class="['edu-navbar-area navbar-area', { 'is-sticky': isSticky }]">
    <!-- <div class="edumim-responsive-nav">
      <div class="container">
        <div class="edumim-responsive-menu">
          <div class="logo">
            <router-link to="/">
              <img src="../../assets/img/logo/logo.svg" alt="logo" />
            </router-link>
          </div>
        </div>
      </div>
    </div> -->
    <div class="edumim-nav">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light">
          <a class="navbar-brand" href="#home">
            <img src="../../assets/img/logo/logo.svg" alt="logo" />
          </a>

          <div
            class="navbar-toggler"
            @click="active = !active"
            :aria-pressed="active ? 'true' : 'false'"
            v-bind:class="{ active: button_active_state }"
            v-on:click="button_active_state = !button_active_state"
          >
            <i class="bx bx-menu"></i>
            <i class="bx bx-x"></i>
          </div>

          <div class="collapse navbar-collapse" :class="{ show: active }">
            <ul class="navbar-nav ms-auto w-100 justify-content-end">
              <li class="nav-item"><a href="#home" class="nav-link">Home</a></li>
              <li class="nav-item"><a href="#about" class="nav-link">About</a></li>
              <li class="nav-item"><a href="#statistics" class="nav-link">Statistics</a></li>
              <li class="nav-item"><a href="#programs" class="nav-link">Program and Modules</a></li>
              <li class="nav-item"><a href="#testimonials" class="nav-link">Testimonials</a></li>
              <li class="nav-item"><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "MainNavbar",
  data() {
    return {
      isSticky: false,
      active: false,
      button_active_state: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", () => {
      const scrollPos = window.scrollY;
      this.isSticky = scrollPos >= 100;
    });
  },
});
</script>

<style scoped>
.navbar-brand img {
  max-width: 65px;
  height: auto;
}
</style>