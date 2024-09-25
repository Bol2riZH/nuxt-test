<script setup lang="ts">
  useHead({
    title: 'My App',
    meta: [{ name: 'description', content: 'My amazing site.' }],
    bodyAttrs: {
      class: 'test',
    },
    script: [{ innerHTML: "console.log('Hello world')" }],
  });

  useSeoMeta({
    title: 'My Amazing Site',
    ogTitle: 'My Amazing Site',
    description: 'This is my amazing site, let me tell you all about it.',
    ogDescription: 'This is my amazing site, let me tell you all about it.',
    ogImage: 'https://example.com/image.png',
    twitterCard: 'summary_large_image',
  });

  const productCategory = ref(1);

  useHead({
    // or as a function
    titleTemplate: productCategory => {
      return productCategory ? `${productCategory} - Site Title` : 'Site Title';
    },
  });
</script>

<template>
  <div>
    <h1 class="text-4xl font-bold">Welcome to the homepage</h1>
    <AppAlert>
      This is an auto-imported component.
      <img src="/img/NuxtJS_Logo.png" alt="Discover Nuxt 3" />
    </AppAlert>
  </div>
</template>

<style>
  .page-enter-active,
  .page-leave-active {
    transition: all 0.2s;
  }
  .page-enter-from,
  .page-leave-to {
    opacity: 0;
    transform: translateY(50%);
  }

  .rotate-enter-active,
  .rotate-leave-active {
    transition: all 0.2s;
  }

  .rotate-enter-from,
  .rotate-leave-to {
    opacity: 0;
    transform: rotate3d(1, 1, 1, 15deg);
  }

  .layout-enter-active,
  .layout-leave-active {
    transition: all 0.4s;
  }
  .layout-enter-from,
  .layout-leave-to {
    filter: grayscale(1);
  }
</style>
