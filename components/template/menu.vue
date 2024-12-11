<template>
  <nav class="font-mono flex-auto max-md:flex-none">
    <ul class="flex justify-start max-md:flex-col">
      <li>
        <NuxtLink to="/" class="p-1 hover:bg-gray-200 dark:hover:bg-gray-600">Main</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about" class="link">About</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/projects" class="link">Projects</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/blog" class="link">Blogs</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
  .link {
    @apply p-1 hover:bg-gray-200 dark:hover:bg-gray-600
  }
</style>
<script setup lang="ts">
</script>