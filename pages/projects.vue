<template>
  <article class="prose dark:prose-invert max-w-none">
    <ContentDoc path="/projects" />
    <ProjectList />
  </article>
</template>

<script setup lang="ts">
import ProjectList from "~/components/content/project-list.vue";
</script>