<script setup lang="ts">
  definePageMeta({
    middleware: 'auth',
  });
  const title = ref('ADMIN');
</script>

<template>
  <div>
    <Head>
      <Title>{{ title }}</Title>
      <Meta name="description" :content="title" />
      <Style type="text/css" children="body { background-color: green; }"></Style>
    </Head>

    <h1 class="text-4xl font-bold">{{ title }}</h1>
  </div>
</template>
