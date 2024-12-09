<template>
  <div>
    <div class="container mx-auto max-w-2xl pt-6">
      <header class="flex justify-between items-center">
        <div>
          <NuxtLink to="/" class="text-xl font-semibold p-2 hover:bg-gray-200">Brian Bronkhorst</NuxtLink>
        </div>
        <TheHeader />
        <ClientOnly>
          <ColorModeSelector />
        </ClientOnly>

      </header>

      <main class="p-2 mt-10">
        <slot />
      </main>
    </div>
  </div>
</template>

<script setup lang="ts">

useHead({
  titleTemplate: '%s - Brian Bronkhorst',
  link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Roboto&display=swap',
      crossorigin: ''
    }
  ]
});
</script>

<style>
 body {
   font-family: 'Roboto';
 }

 body {
   @apply bg-white dark:bg-gray-900 text-gray-700 dark:text-gray-300
 }
</style>