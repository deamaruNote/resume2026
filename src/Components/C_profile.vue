<script setup lang="ts">
const num = 10;
</script>

<template>
  <div class="m-box">
      <div v-for="n in num" :key="n" class="box">
      {{ n }}
      </div>
  </div>
</template>

<style scoped>
.m-box {
    display: flex;
    justify-content: flex-start;
    margin: 0 auto;
    width: 80%;
    gap: 13px;
    align-items: baseline;
    flex-wrap: wrap;
}
.box {
  width: calc(25% - 10px);
  aspect-ratio: 1;
  background: #000000;
}
@media (max-width: 760px) {
    .box{
        width: calc(50% - 7px);
    }
}
@media (max-width: 480px){
    .box{
        width: 100%;
    }
}
</style>
