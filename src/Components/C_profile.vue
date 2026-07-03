<script setup lang="ts">
import VueLazyload from 'vue3-lazyload'
const count = 9;
const url_ary = [
  "https://deamarunote.github.io/demo-store2/",
  "https://deamarunote.github.io/coffee-store/",
  "https://www.maisonbest.com.tw/",
  "https://deamarunote.github.io/vue3-practise/#/",
  "https://deamarunote.github.io/F2E_week/",
  "https://deamarunote.github.io/F2e_2022_3week/",
  "http://www.wao-design.com/",
  "",
  "",
];
</script>

<template>
  <div class="m-box">
    <a
      v-for="n in count"
      :key="n"
      class="box"
      :href="url_ary[n]"
      target="_blank"
      :style="{ animationDelay: `${(n - 1) * 0.15}s` }"
    >
      <img
        :src="`project_${n}.png`"
        :alt="`project_${n}`"
        loading="lazy"
        decoding="async"
      />
    </a>
  </div>
</template>

<style scoped>
.m-box {
  display: flex;
  justify-content: flex-start;
  margin: 0 auto;
  width: 80%;
  gap: 20px;
  align-items: baseline;
  flex-wrap: wrap;
}
.box {
  position: relative;
  width: calc(20% - 20px);
  aspect-ratio: 1;
  background: #000000;
  overflow: hidden;
}
.box::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  z-index: 10;
  width: 100%;
  height: 100%;
  background: #000000;
  opacity: 0.3;
  transition: all 0.5s;
}
.box:hover::before {
  opacity: 0;
}
@keyframes boxIn {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
.box:hover img {
  transform: translateX(-60px) scale(1.2);
  animation: boxIn 0.6s ease-in forwards;
  animation-delay: 2s;
}
.box img {
  transform: translateX(-20%);
  height: 100%;
  transition: all 0.5s;
}
@media (max-width: 760px) {
  .box {
    width: calc(50% - 10px);
  }
}
@media (max-width: 480px) {
  .box {
    width: 100%;
  }
}
</style>
