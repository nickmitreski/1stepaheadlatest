<template>
  <footer class="edu-footer-area">
    <div class="container">
      <div class="footer-top-area ptb-100">
        <div class="row justify-content-center text-center text-lg-start">
          <div class="col-lg-4 col-md-6 col-sm-12 mb-4 mb-lg-0 d-flex flex-column align-items-center align-items-lg-start">
            <div class="single-footer-widget w-100">
              <router-link to="/" class="logo mb-3">
                <img src="../../assets/img/logo/footer-logo.svg" alt="1 Step Ahead logo" />
              </router-link>
              <p class="footer-desc">
                1 Step Ahead empowers young Australians with practical financial literacy and wellbeing skills for a brighter future.
              </p>
              <ul class="social-links d-flex justify-content-center justify-content-lg-start">
                <li>
                  <a href="#" target="_blank">
                    <i class="bx bxl-facebook"></i>
                  </a>
                </li>
                <li>
                  <a href="#" target="_blank">
                    <i class="bx bxl-instagram"></i>
                  </a>
                </li>
                <li>
                  <a href="#" target="_blank">
                    <i class="bx bxl-linkedin"></i>
                  </a>
                </li>
              </ul>
            </div>
          </div>
          <div class="col-lg-3 offset-lg-1 col-md-6 col-sm-6 mb-4 mb-lg-0 d-flex flex-column align-items-center align-items-lg-start">
            <div class="single-footer-widget w-100">
              <h3>Quick Links</h3>
              <ul class="links-list">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#statistics">Statistics</a></li>
                <li><a href="#programs">Program and Modules</a></li>
                <li><a href="#testimonials">Testimonials</a></li>
                <li><a href="#contact">Contact</a></li>
              </ul>
            </div>
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 d-flex flex-column align-items-center align-items-lg-start">
            <div class="single-footer-widget w-100">
              <h3>Legal</h3>
              <ul class="links-list">
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">ABN: 12 345 678 910</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="pr-line"></div>
      <div class="footer-bottom-area">
        <p class="created-by centered">
          Created by Flash Forward Digital
        </p>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainFooter",
  setup() {
    const currentYear = ref(new Date().getFullYear());

    return {
      currentYear,
    };
  },
});
</script>

<style scoped>
.logo img {
  max-width: 120px;
  height: auto;
}
.footer-bottom-area {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 18px 0 0 0;
}
.created-by {
  color: #fff;
  font-size: 20px;
  font-weight: 600;
  margin: 0;
  width: 100%;
  text-align: center;
}
.footer-desc {
  margin-bottom: 24px;
}
@media (max-width: 991px) {
  .footer-bottom-area {
    flex-direction: column;
    text-align: center;
    gap: 10px;
  }
  .created-by {
    margin: 0;
  }
  .footer-top-area .row > div {
    margin-bottom: 32px;
  }
}
</style>