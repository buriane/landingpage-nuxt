<script lang="ts" setup>
definePageMeta({
  layout: 'page',
})

useSeoMeta({
  title: 'About Me',
})
</script>

<template>
  <PageContainer class="py-6">
    <h1 class="text-2xl font-bold">About</h1>
    <NuxtImg src="https://images.unsplash.com/photo-1623282033815-40b05d96c903?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="About Image" class="mt-4 rounded-lg shadow-lg" />
  </PageContainer>
</template>