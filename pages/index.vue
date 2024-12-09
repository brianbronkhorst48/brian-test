<template>
  <div>
    <div>
      <h2>Content</h2>
    </div>
  </div>
</template>

<script setup lang="ts">
useSeoMeta({
  title: 'Main page',
  ogTitle: 'Main page',
  description: 'This is my amazing site, let me tell you all about it.',
  ogDescription: '[og:description]',
  ogImage: '[og:image]',
  ogUrl: '[og:url]',
  twitterTitle: 'Main page',
  twitterDescription:'[twitter:description]',
  twitterImage: '[twitter:image]',
  twitterCard: 'summary',
})
useHead({
  htmlAttrs: {
    lang: 'en'
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/favicon.png'
    }
  ]
})
</script>
