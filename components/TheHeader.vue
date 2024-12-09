<template>
  <nav class="font-mono flex-auto">
    <ul class="flex space-x-4 justify-start ml-5">
      <li>
        <NuxtLink to="/" class="p-1 hover:bg-gray-200">Main</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about" class="link">About</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/projects" class="link">Projects</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
  .link {
    @apply p-1 hover:bg-gray-200
  }
</style>
<script setup lang="ts">
</script>