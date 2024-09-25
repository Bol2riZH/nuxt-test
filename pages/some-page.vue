<script setup lang="ts">
  definePageMeta({
    pageTransition: {
      name: 'bounce',
      mode: 'out-in', // default
    },
  });
</script>

<template>
  <section>
    <h1 class="text-4xl font-bold">Some Page</h1>
    <p>This page will be displayed at the /some-page route.</p>
  </section>
</template>
