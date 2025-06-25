<template>
  <div class="edu-banner-area banner01">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 col-md-12">
          <div class="edu-banner-content">
            <h1 class="hero-title">
              <span class="shape02">Empowering</span> Teens & Young Adults
            </h1>
            <p class="hero-subtitle">
              Helping the next generation take control of their financial future and mental health.
            </p>
          </div>
        </div>
        <div class="col-lg-6 col-md-12">
          <div class="edu-banner-image">
            <img src="../../assets/img/banner/man1.png" alt="banner-img" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "MainBanner",
});
</script>

<style scoped>
.hero-title {
  margin-bottom: 12px;
}
.hero-subtitle {
  margin-top: 0;
}
</style>