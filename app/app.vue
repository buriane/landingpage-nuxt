<script lang="ts" setup>
  useSeoMeta({
    titleTemplate: '%s - My Application',
  })
</script>

<template>
  <div>
    <NuxtLoadingIndicator color="red" :throttle="0" />
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
