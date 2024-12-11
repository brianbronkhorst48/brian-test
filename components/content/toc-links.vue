<template>
  <ul class="list-none ml-0 p-0">
    <li class="no-underline" v-for="link in links" :key="link.id">
      <NuxtLink :to="{ path: route.path, hash: `#${link.id}` }" :class="{'ml-0 no-underline': level}">
          {{ link.text }}
      </NuxtLink>
      <TocLinks :links="link.children" :level="level + 1" />
    </li>
  </ul>
</template>

<script setup>
const route = useRoute()
defineProps({
  links: Array,
  level: {
    type: Number,
    default: 0
  }
})
</script>