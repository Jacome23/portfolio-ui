<template>
  <q-btn :href="link" :icon="icon" size="xl" :label="label" />
</template>

<script setup lang="ts">
defineOptions({
  name: 'EssentialIcons',
});

export interface EssentialIconProps {
  icon?: string;
  link?: string;
  label?: string;
}

withDefaults(defineProps<EssentialIconProps>(), {
  icon: '',
  link: '#',
  label: '',
});
</script>

<style scoped>
.sidebarNav {
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: bold;
}
</style>
