<!-- Exit Icon - Vue component for module 'nuxt-icon' needs to be inside components/global/ folder -->
<script setup lang="ts">
import { defineComponent } from 'vue';

defineComponent({
  name: 'ExitIcon',
});
</script>
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
    <g fill="currentColor">
      <path fill-rule="evenodd"
        d="M11 20a1 1 0 0 0-1-1H5V5h5a1 1 0 1 0 0-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h5a1 1 0 0 0 1-1"
        clip-rule="evenodd" />
      <path
        d="M21.714 12.7a.996.996 0 0 0 .286-.697v-.006a.997.997 0 0 0-.293-.704l-4-4a1 1 0 1 0-1.414 1.414L18.586 11H9a1 1 0 1 0 0 2h9.586l-2.293 2.293a1 1 0 0 0 1.414 1.414l4-4z" />
    </g>
  </svg>
</template>