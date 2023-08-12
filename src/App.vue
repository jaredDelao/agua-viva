<script setup>
import Principal from './components/Principal.vue'
import Video from './components/Video.vue'
import Steps from './components/steps.vue';
import Slider from './components/Slider.vue';
import Community from './components/Community.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <div class="main">
    <div class="max-wrapper">
      <Principal />
      <Video />
      <Steps />
    </div>
    <Slider />
    <Community />
    <Footer />
  </div>
</template>

<style scoped>
.main {
  height: 100%;
}

.max-wrapper {
  max-width: 1000px;
  width: 100%;
  margin: auto;
}
</style>
