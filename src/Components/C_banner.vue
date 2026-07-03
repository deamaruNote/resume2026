<script setup lang="ts">
const main_color = "#233A58";
</script>

<template>
  <div>
    <div class="box-icon">
      <div class="img">
        <svg
          width="54"
          height="40"
          viewBox="0 0 54 40"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M46.7874 29.7574C49.766 29.7574 52.2002 32.0809 52.3801 35.0143H52.384V35.0602C52.3894 35.1603 52.3928 35.2614 52.3928 35.3629C52.3928 35.4638 52.3893 35.5641 52.384 35.6637V39.4635C52.388 39.5779 52.3928 39.6928 52.3928 39.8082C52.3928 39.9233 52.388 40.0379 52.384 40.152V40.7975H52.343C51.8475 45.6701 47.7313 49.4723 42.7278 49.4723C37.7244 49.4721 33.609 45.6699 33.1135 40.7975H33.0637V35.0143H33.0754C33.2553 32.0809 35.6905 29.7574 38.6692 29.7574H46.7874Z"
            :fill="main_color"
          />
          <path
            d="M10.5111 29.2497C10.7608 29.2492 11.0213 29.2487 11.2924 29.2487C17.6294 29.2489 22.7777 34.3314 22.8861 40.6423H22.89V47.5593H22.8881C22.8882 47.5703 22.889 47.5814 22.889 47.5925C22.889 48.9224 21.8108 50.0007 20.4808 50.0007H7.54333C4.78196 50.0007 2.54341 47.762 2.54333 45.0007V32.7224C2.54333 30.9354 3.89284 29.4632 5.6283 29.2702V29.2487H10.5111V29.2497Z"
            :fill="main_color"
          />
          <path
            d="M42.5688 0.000976562C48.0946 0.0608499 52.5809 7.37239 53.3373 16.4482C53.4811 18.173 52.3676 19.7274 50.3364 19.7275H34.7329C32.7014 19.7275 31.5881 18.1731 31.7319 16.4482C32.4883 7.37215 36.9744 0.0604401 42.5004 0.000976562V0H42.5688V0.000976562Z"
            :fill="main_color"
          />
          <path
            d="M19.5342 0C23.7001 0 27.0771 5.28224 27.0771 11.7979C27.0771 18.9756 26.4712 19.4956 22.8223 19.5293V19.5332H4.25488L4.25391 19.5293C0.60612 19.4955 1.66353e-05 18.9747 0 11.7979C0 5.28226 3.37709 3.60607e-05 7.54297 0C9.9882 0 12.1598 1.82072 13.5381 4.6416C14.9163 1.82054 17.0889 0.000153907 19.5342 0Z"
            :fill="main_color"
          />
        </svg>
      </div>
      <h1>Website Devloper</h1>
    </div>
  </div>
</template>

<style scoped>
.box-icon {
  padding: 10px;
  width: var(--box-width);
  height: var(--box-width);
  background: var(--min-color);
  box-sizing: border-box;
}
h1 {
  position: absolute;
  color: var(--min-color);
  transform: translate(-30%, -40px) rotate(-3deg);
  font-size: 70px;
  font-weight: 300;
  font-family: Dancing Script, cursive;
  mix-blend-mode: difference;
  z-index: 300;
  animation: h1_start 1.5s ease-in-out forwards;
}
.box-icon::before {
  content: "";
  position: fixed;

  width: 300vmax;
  height: 300vmax;
  left: 50%;
  top: 150px;

  transform: translate(-50%, -50%) scale(1);
  background: var(--min-color);
  z-index: 200;
  animation: bg_start 1.5s ease-in-out forwards;
  animation-delay: 0.3s;
}

.img {
  margin: 0 0 0 auto;
  width: 20px;
  aspect-ratio: 1;
  transform: translate(0, -10px);
}
.img > svg {
  width: 100%;
  padding: 0;
}
/* RWD */
@media (max-width: 480px) {
  h1 {
    font-size: 2.5rem;
    transform: translate(-2.5rem, -1rem) rotate(-3deg);
  }
  .img {
    margin: auto;
    transform: scale(7) translate(0, 0.5rem);
  }
}

/* ANIMATION */
@keyframes h1_start {
  0% {
    scale: 3;
    rotate: 363deg;
  }

  100% {
    scale: 1;
    rotate: -3deg;
  }
}
@keyframes bg_start {
  0% {
    transform: translate(-50%, -50%) scale(1);
    opacity: 1;
  }

  85% {
    transform: translate(-50%, -50%) scale(0.03);
    opacity: 1;
  }

  100% {
    transform: translate(-50%, -50%) scale(0);
    opacity: 0;
  }
}
</style>