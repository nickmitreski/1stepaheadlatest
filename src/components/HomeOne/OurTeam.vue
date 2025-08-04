<template>
  <div class="edu-about-area ptb-100 team-background">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 col-md-12">
          <div class="edu-about-content">
            <h2>
              <span class="shape02">Our</span> Team
            </h2>
            <p>
              Our programs are co-facilitated by experts in:
            </p>
            <div class="team-expertise">
              <div class="expertise-item">
                <div class="icon">
                  <img src="../../assets/img/svg/check_blue.svg" alt="check" />
                </div>
                <span>Financial literacy and tax systems</span>
              </div>
              <div class="expertise-item">
                <div class="icon">
                  <img src="../../assets/img/svg/check_blue.svg" alt="check" />
                </div>
                <span>Youth mental health and psychology</span>
              </div>
              <div class="expertise-item">
                <div class="icon">
                  <img src="../../assets/img/svg/check_blue.svg" alt="check" />
                </div>
                <span>Education and behaviour change</span>
              </div>
            </div>
            <p>
              We create safe, engaging spaces where young people can learn without judgement and walk away with real tools for life.
            </p>
            
            <h2 class="mt-5">
              <span class="shape02" style="color: #00D1B2;">Our</span> Values
            </h2>
            <div class="team-values">
              <div class="value-item">
                <div class="icon">
                  <img src="../../assets/img/svg/check.svg" alt="check" />
                </div>
                <span><strong style="color: #00D1B2;">Empower</strong> – through education and self-awareness</span>
              </div>
              <div class="value-item">
                <div class="icon">
                  <img src="../../assets/img/svg/check.svg" alt="check" />
                </div>
                <span><strong style="color: #00D1B2;">Trust</strong> – in the way we teach, lead, and support</span>
              </div>
              <div class="value-item">
                <div class="icon">
                  <img src="../../assets/img/svg/check.svg" alt="check" />
                </div>
                <span><strong style="color: #00D1B2;">Growth</strong> – as lifelong learners, individuals, and communities</span>
              </div>
              <div class="value-item">
                <div class="icon">
                  <img src="../../assets/img/svg/check.svg" alt="check" />
                </div>
                <span><strong style="color: #00D1B2;">Motivation</strong> – to take action and stay 1 step ahead</span>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-6 col-md-12">
          <div class="edu-about-image">
            <img src="../../assets/img/all-img/t1.png" alt="team-img" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "OurTeam",
};
</script>

<style scoped>
.team-background {
  background-image: url('../../assets/img/banner/3.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  min-height: 600px; /* Ensure the section has enough height */
}

.team-background .container {
  position: relative;
  z-index: 2;
}

.team-expertise,
.team-values {
  margin: 20px 0;
}

.expertise-item,
.value-item {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}

.expertise-item .icon,
.value-item .icon {
  margin-right: 12px;
  flex-shrink: 0;
}

.expertise-item .icon img,
.value-item .icon img {
  width: 20px;
  height: 20px;
}

.expertise-item span,
.value-item span {
  font-size: 16px;
  color: var(--paragraphColor);
  line-height: 1.5;
}

.value-item span strong {
  color: var(--mainColor);
}
</style> 