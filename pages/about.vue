<script setup lang="ts">
  definePageMeta({
    pageTransition: {
      name: 'rotate',
    },
    layout: 'orange',
    layoutTransition: {
      name: 'slide-in',
    },
  });
</script>

<template>
  <section>
    <h1 class="text-4xl font-bold">About</h1>
    <p>This page will be displayed at the /about route.</p>
  </section>
</template>
