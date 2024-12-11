<template>
  <div>
    <div>
      <h1 class="font-extrabold text-2xl">Homepage</h1>
      <p class="mt-4"> Welcome to my portfolio!</p>
      <ul class="list-disc pl-5">
        <li class="pt-2">
          <NuxtLink to="/projects" class="p-1 hover:underline hover:dark:text-gray-100">See my projects</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/blog" class="p-1 hover:underline hover:dark:text-gray-100">See my blogs</NuxtLink>
        </li>
      </ul>
      <article class="prose dark:prose-invert prose-h1:text-2xl max-w-none">
        <ContentDoc path="/" />
      </article>
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
