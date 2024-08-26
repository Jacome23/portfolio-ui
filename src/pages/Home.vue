<template>
  <!-- <div id="main" class="row"> -->
  <!-- <div class="col">
      <img src="../../public/pictures/profile.jpg" alt="profile" />
    </div> -->
  <!-- <div class="col"> -->
  <div class="row">
    <div class="resume-header">James Nunieza</div>
  </div>
  <div class="row">
    <div class="resume-caption">Full Stack Web Developer</div>
  </div>
  <div class="row">
    <div class="resume-profile">
      I have a degree in Electronics Engineering. Right now I'm currently
      focusing on web development related work. I specialize in creating web
      apps that help people transform their data into a more understandable
      forms.
    </div>
    <div class="row">
      <div class="q-pa-md q-gutter-lg">
        <q-btn
          target="”_blank”"
          href="https://github.com/Jacome23"
          color="black"
          icon="code"
          size="xl"
          label="github"
        />

        <q-btn
          color="white"
          size="xl"
          text-color="black"
          icon="assured_workload"
          label="my works"
          @click="fullWidth = true"
        />

        <q-btn
          href="https://drive.google.com/file/d/1Bq24NyqJ73rIneAq3D9gNpZz5LhZ2kJ-/view?usp=sharing"
          target="”_blank”"
          color="black"
          size="xl"
          text-color="white"
          icon="assignment_turned_in"
          label="resume"
        />
      </div>
    </div>
  </div>
  <q-dialog
    v-model="fullWidth"
    full-width
    full-height
    backdrop-filter="blur(4px)"
  >
    <q-card>
      <q-toolbar class="bg-orange">
        <q-toolbar-title>
          <div style="color: white">MY WORKS</div>
        </q-toolbar-title>
        <q-btn flat color="white" v-close-popup round dense icon="close" />
      </q-toolbar>
    </q-card>
  </q-dialog>
</template>

<script setup lang="ts">
import { ref } from 'vue';

defineOptions({
  name: 'HomePage',
});

const fullWidth = ref(false);
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
