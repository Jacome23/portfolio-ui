<template>
  <div class="row">
    <div class="resume-header">About</div>
  </div>
  <!-- <div class="row">
    <div class="resume-caption">Full Stack Web Developer</div>
  </div> -->
  <div class="row">
    <div class="resume-profile">
      This is my portfolio website. Although it's currently in development, I do
      hope it catches your eye. Thanks :)
    </div>
  </div>
</template>

<script setup lang="ts">
// import { ref } from 'vue';

defineOptions({
  name: 'HomePage',
});

// const fullWidth = ref(false);
</script>

<style>
.image-profile {
  background-image: url('../../public/pictures/profile.jpg');
  background-repeat: no-repeat;
  background-size: contain;
}

.resume-header {
  font-size: 80px;
  font-weight: bold;
}

.resume-caption {
  margin-bottom: 20px;
  font-size: 40px;
}

.resume-profile {
  margin-bottom: 20px;
  font-size: 30px;
}
</style>
