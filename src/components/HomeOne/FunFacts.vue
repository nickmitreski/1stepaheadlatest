<template>
  <div class="edu-counter-area stats-bg">
    <div class="container">
      <div class="edu-section-title stats-title-underline">
        <h2>Statistics</h2>
      </div>
      <div class="circle-stats-row">
        <div class="stat-circle-graph" v-for="stat in stats" :key="stat.percent">
          <svg viewBox="0 0 200 200" class="circle-svg">
            <!-- White arc to complete the circle -->
            <path
              :d="describeArc(100, 100, 90, stat.percent * 3.6, 360)"
              fill="none"
              stroke="#fff"
              stroke-width="20"
              stroke-linecap="round"
            />
            <!-- Foreground arc (percentage) -->
            <path
              :d="describeArc(100, 100, 90, 0, stat.percent * 3.6)"
              fill="none"
              :stroke="stat.color"
              stroke-width="20"
              stroke-linecap="round"
            />
          </svg>
          <div class="stat-text compact-text">
            <div class="stat-percent" :style="{ color: stat.color }">{{ stat.percent }}%</div>
            <div class="stat-desc">{{ stat.text }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Helper to describe an SVG arc (for open gauge)
function describeArc(cx, cy, r, startAngle, endAngle) {
  const start = polarToCartesian(cx, cy, r, endAngle);
  const end = polarToCartesian(cx, cy, r, startAngle);
  const arcSweep = endAngle - startAngle <= 180 ? "0" : "1";
  // If drawing a full circle, need to use two arcs (SVG limitation)
  if (Math.abs(endAngle - startAngle) >= 360) {
    const midAngle = startAngle + 180;
    const mid = polarToCartesian(cx, cy, r, midAngle);
    return [
      "M", start.x, start.y,
      "A", r, r, 0, 1, 0, mid.x, mid.y,
      "A", r, r, 0, 1, 0, end.x, end.y
    ].join(" ");
  }
  return [
    "M", start.x, start.y,
    "A", r, r, 0, arcSweep, 0, end.x, end.y
  ].join(" ");
}
function polarToCartesian(cx, cy, r, angleInDegrees) {
  const angleInRadians = (angleInDegrees - 90) * Math.PI / 180.0;
  return {
    x: cx + (r * Math.cos(angleInRadians)),
    y: cy + (r * Math.sin(angleInRadians))
  };
}
const stats = [
  {
    percent: 64,
    text: 'Australians report low satisfaction in their lives due to financial stress',
    color: 'var(--mainColor)',
  },
  {
    percent: 15,
    text: 'of females and 27% of males graduate from Australian High schools financially literate',
    color: 'var(--secounderyColor)',
  },
  {
    percent: 45,
    text: 'of the total Australian population (more than 8.5 million people) are financially illiterate',
    color: 'var(--mainColor)',
  },
  {
    percent: 90,
    text: 'of women will retire with inadequate savings to fund a comfortable lifestyle',
    color: 'var(--secounderyColor)',
  },
];
</script>

<style scoped>
.edu-counter-area.stats-bg {
  background: url('@/assets/img/all-img/stats_bg.png') repeat center center;
  background-size: cover;
  padding: 50px 0;
  background-color: transparent !important;
}
.edu-section-title {
  max-width: 750px;
  position: relative;
  text-align: center;
  margin-bottom: 40px;
  margin-right: auto;
  margin-top: -7px;
  margin-left: auto;
}
.edu-section-title h2 {
  margin-bottom: 0;
  font-size: 44px;
  color: var(--blackColor);
  font-family: var(--fontFamily);
}
.stats-title-underline h2 {
  position: relative;
  display: inline-block;
  padding-bottom: 8px;
}
.stats-title-underline h2::after {
  content: '';
  display: block;
  width: 60px;
  height: 4px;
  background: var(--secounderyColor);
  border-radius: 2px;
  margin: 10px auto 0 auto;
}
.circle-stats-row {
  display: flex;
  flex-wrap: nowrap;
  justify-content: center;
  align-items: flex-start;
  margin-top: 32px;
  margin-bottom: 48px;
  gap: 80px;
}
.stat-circle-graph {
  position: relative;
  width: 260px;
  height: 260px;
  margin: 0;
  font-family: var(--fontFamily);
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  flex-shrink: 0;
}
.circle-svg {
  width: 100%;
  height: 100%;
  display: block;
}
.stat-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  width: 85%;
  font-family: var(--fontFamily);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0 8px;
}
.stat-text.compact-text {
  width: 65%;
  max-width: 170px;
}
.stat-percent {
  font-size: 36px;
  font-weight: 800;
  margin-bottom: 10px;
  line-height: 1;
  letter-spacing: -1px;
}
.stat-desc {
  font-size: 14px;
  color: var(--blackColor);
  font-weight: 700;
  margin: 0;
  line-height: 1.35;
  word-break: break-word;
}
.green-accent {
  box-shadow: none;
}
@media (max-width: 1200px) {
  .stat-circle-graph {
    width: 200px;
    height: 200px;
  }
  .stat-percent {
    font-size: 28px;
  }
  .stat-desc {
    font-size: 12px;
  }
}
@media (max-width: 991px) {
  .circle-stats-row {
    flex-wrap: wrap;
    flex-direction: row;
    gap: 24px;
  }
  .stat-circle-graph {
    width: 140px;
    height: 140px;
    margin-bottom: 24px;
  }
  .stat-percent {
    font-size: 18px;
  }
  .stat-desc {
    font-size: 10px;
  }
}
@media (max-width: 767px) {
  .circle-stats-row {
    flex-direction: column;
    align-items: center;
    gap: 0;
  }
  .stat-circle-graph {
    width: 100px;
    height: 100px;
    margin-bottom: 18px;
  }
}
</style>