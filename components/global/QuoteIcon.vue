<!-- Quote Icon - Vue component for module 'nuxt-icon' needs to be inside components/global/ folder -->
<script setup lang="ts">
import { defineComponent } from 'vue';

defineComponent({
  name: 'QuoteIcon',
});
</script>
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 36 36">
    <path fill="currentColor"
      d="M11.86 16.55a4.31 4.31 0 0 0-2.11.56a14.44 14.44 0 0 1 4.36-6a1.1 1.1 0 0 0-1.4-1.7c-4 3.25-5.78 7.75-5.78 10.54A5.08 5.08 0 0 0 10 24.58a4.4 4.4 0 0 0 1.88.44a4.24 4.24 0 1 0 0-8.47Z"
      class="clr-i-outline clr-i-outline-path-1" />
    <path fill="currentColor"
      d="M23 16.55a4.29 4.29 0 0 0-2.11.56a14.5 14.5 0 0 1 4.35-6a1.1 1.1 0 1 0-1.39-1.7c-4 3.25-5.78 7.75-5.78 10.54a5.08 5.08 0 0 0 3 4.61A4.37 4.37 0 0 0 23 25a4.24 4.24 0 1 0 0-8.47Z"
      class="clr-i-outline clr-i-outline-path-2" />
    <path fill="none" d="M0 0h36v36H0z" />
  </svg>
</template>