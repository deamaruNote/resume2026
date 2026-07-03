<script setup lang="ts">
  import Banner from './C_banner.vue';
  import Profile from './C_profile.vue';
  import Footer from './C_footer.vue'
</script>

<template>
  <div class="m-body">
    <Banner class="box_b" />
    <Profile class="box_p" />
    <Footer />
  </div>
</template>

<style>
  .m-body{
    text-align: center;
    width: 100vw;
    margin: 0;
    padding: 0;
  }
  .box_b, .box_p{
    display: flex;
    width: 100%;
    justify-content: center;
    align-items: center;
  }
  .box_b{
    min-height: auto;
    height: 300px;
    margin-bottom: 50px;
  }
</style>
