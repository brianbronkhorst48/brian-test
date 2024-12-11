<template>
  <div class="container mx-auto max-w-4xl">
    <div class="container mx-auto max-w-2xl pt-6">
      <header class="flex justify-between items-center max-md:flex-col max-md:items-start">
        <div class="w-full block">
          <NuxtLink to="/" class="text-xl font-semibold pt-2 pl-1 hover:bg-gray-200 dark:hover:bg-gray-600">Brian Bronkhorst</NuxtLink>
        </div>
        <Menu />
        <ClientOnly>
          <ColorMode />
        </ClientOnly>

      </header>

      <main class="p-2 mt-10">
        <slot />
      </main>
    </div>
  </div>
</template>

<script setup lang="ts">

import Menu from "~/components/template/menu.vue";
import ColorMode from "~/components/template/colorMode.vue";

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