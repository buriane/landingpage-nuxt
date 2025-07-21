<script lang="ts" setup>
const menus = ref([
  { label: 'Home', to: '/' },
  { label: 'About', to: '/about' },
]);
</script>

<template>
  <div class="bg-gray-50 text-gray-800 dark:bg-gray-950 dark:text-gray-100 min-h-screen flex flex-col">
    <header
      class="sticky top-0 w-full z-30 dark:bg-gray-950/70 dark:text-gray-100/70 border-b border-gray-500/50 h-[68px] flex backdrop-blur-lg">
      <PageContainer class="flex-1 flex items-center justify-between">
        <NuxtLink to="/" class="font-bold text-lg">Landing Page</NuxtLink>
        <div class="flex divide-x-2 gap-4 divide-gray-500/50 items-center">
          <nav>
            <ul class="flex gap-4">
              <li v-for="(menu, i) in menus" :key="i">
                <NuxtLink :to="menu.to" class="hover:text-primary-500">{{ menu.label }}</NuxtLink>
              </li>
            </ul>
          </nav>
          <div class="pl-4">
            <ToggleMode />
          </div>
        </div>
      </PageContainer>
    </header>

    <main class="flex-1 flex">
      <slot />
    </main>

    <footer class="border-t border-gray-500/50 h-[48px] flex">
      <PageContainer class="flex-1 flex items-center justify-between">
        <div class="flex-1">
          <span class="text-sm">&copy; 2025 My Application. All rights reserved.</span>
        </div>
        <div>
          <Icon name="i-heroicons:heart" class="text-primary" />
        </div>
      </PageContainer>
    </footer>
  </div>
</template>