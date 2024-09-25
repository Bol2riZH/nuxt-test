<script setup lang="ts">
  const route = useRoute();
  // When accessing /posts/1, route.params.id will be 1
  console.log(route.params.id);

  definePageMeta({
    validate: async route => {
      // Check if the id is made up of digits
      return typeof route.params.id === 'string' && /^\d+$/.test(route.params.id);
    },
  });
</script>

<template>
  <div>
    <h1 class="text-4xl font-bold">Post {{ route.params.id }}</h1>
  </div>
</template>
