<template>
  <q-layout view="lHh Lpr lFf" class="center">
    <q-header elevated class="header-color">
      <q-toolbar>
        <!-- <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        /> -->

        <q-toolbar-title style="font-weight: bold"
          >James Nunieza</q-toolbar-title
        >
        <!-- <div style="flex-grow: 1" /> -->
        <EssentialIcons
          v-for="(item, index) of icons"
          :key="`${index}-${item}`"
          v-bind="item"
        />
      </q-toolbar>
    </q-header>

    <!-- <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> </q-item-label>

        <EssentialLink
          v-for="link in linksList"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <q-page-container>
      <div class="row">
        <div class="col">
          <img src="/pictures/profile.jpg" alt="profile" />
        </div>
        <div class="col">
          <router-view />
        </div>
      </div>
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import EssentialIcons, {
  EssentialIconProps,
} from 'components/EssentialIcons.vue';

defineOptions({
  name: 'MainLayout',
});

const icons: EssentialIconProps[] = [
  {
    label: 'Home',
    icon: 'home',
    link: '#home',
  },
  {
    label: 'About',
    icon: 'help',
    link: '#home/about',
    // link: 'About',
  },
  {
    label: 'Skills',
    icon: 'pan_tool',
  },
  {
    // title: 'school',
    // link: 'https://youtube.com',
    label: 'Portfolio',
    icon: 'article',
  },
  {
    // title: 'school',
    // link: 'https://youtube.com',
    label: 'Contact',
    icon: 'call',
  },
];

// const linksList: EssentialLinkProps[] = [
// {
//   title: 'Docs',
//   caption: 'quasar.dev',
//   icon: 'school',
//   link: 'quasar.dev',
// },
// {
//   title: 'Github',
//   caption: 'https://github.com/Jacome23',
//   icon: 'code',
//   link: 'https://github.com/Jacome23',
// },
// {
//   title: 'Discord Chat Channel',
//   caption: 'chat.quasar.dev',
//   icon: 'chat',
//   link: 'https://chat.quasar.dev',
// },
// {
//   title: 'Forum',
//   caption: 'forum.quasar.dev',
//   icon: 'record_voice_over',
//   link: 'https://forum.quasar.dev',
// },
// {
//   title: 'Twitter',
//   caption: '@quasarframework',
//   icon: 'rss_feed',
//   link: 'https://twitter.quasar.dev',
// },
// {
//   title: 'Facebook',
//   caption: '@QuasarFramework',
//   icon: 'public',
//   link: 'https://facebook.quasar.dev',
// },
// {
//   title: 'Quasar Awesome',
//   caption: 'Community Quasar projects',
//   icon: 'favorite',
//   link: 'https://awesome.quasar.dev',
// },
// ];

// const leftDrawerOpen = ref(false);

// function toggleLeftDrawer() {
//   leftDrawerOpen.value = !leftDrawerOpen.value;
// }
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}
.header-color {
  background-color: black;
}
.center {
  display: flex;
  justify-content: center;
  align-items: center;
}

img {
  max-width: 100%;
  height: auto;
  border-radius: 50%;
}
</style>
