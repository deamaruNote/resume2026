<script setup lang="ts">
import '@fortawesome/fontawesome-free/css/all.min.css'
</script>

<template>
  <div class="footer">
    <!-- ENG -->
    <a href="https://github.com/deamaruNote" target="_blank" class="icon">
      <i class="fa-brands fa-github"></i>
    </a>
    <a href="https://hackmd.io/@Marude" target="_blank" class="icon">
      <i class="fa-solid fa-book"></i>
    </a>
    <!-- UI/UX -->
    <a href="https://www.behance.net/deamaru" target="_blank" class="icon">
      <i class="fa-brands fa-behance"></i>
    </a>
    <!-- <a href="https://heyzine.com/flip-book/5aa43bc172.html#page/1" target="_blank" class="icon">
      <i class="fa-regular fa-address-book"></i>
    </a> -->
    <br>
    <span>copyright © all rights reserved</span>
  </div>
</template>

<style scoped>
.footer {
    text-align: center;
    height: 80px;
    gap: 20px;
    margin: 50px auto;
}
.icon {
    display: inline-block;
    width: 16px;
    height: 16px;
    font-size: 18px;
    padding: 20px 5px;
    color: var(--min-color);
}
</style>
