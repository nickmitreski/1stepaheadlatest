<template>
  <div class="edu-about-area ptb-100">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 col-md-12">
          <div class="edu-about-image">
            <img src="../../assets/img/all-img/about1.png" alt="banner-img" />
          </div>
        </div>
        <div class="col-lg-6 col-md-12">
          <div class="edu-about-content">
            <p class="sub-title">About 1 Step Ahead</p>
            <h2>
              <span class="shape02">Empowering</span> Young Australians for Financial Wellbeing
            </h2>
            <p>
              At 1 Step Ahead, we help teens and young adults build financial and emotional balance for a brighter future.
            </p>
            <div class="about-list">
              <div class="items">
                <div class="about-single-content">
                  <div class="icon2">
                    <img src="../../assets/img/svg/light.svg" alt="icon" />
                  </div>
                  <div class="content">
                    <h3>Our Vision</h3>
                    <p>
                      To be the catalyst for transforming lives through financial wellbeing education around Australia.
                    </p>
                  </div>
                </div>
              </div>
              <div class="items">
                <div class="about-single-content">
                  <div class="icon2">
                    <img src="../../assets/img/svg/target.svg" alt="icon" />
                  </div>
                  <div class="content">
                    <h3>Our Mission</h3>
                    <p>
                      To help young Australians comprehend how our emotions shape our financial behaviours.
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <router-link to="/about" class="default-btn">
              Meet Our Founders
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutUs",
};
</script>