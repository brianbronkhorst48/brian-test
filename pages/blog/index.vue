<template>
  <section class="not-prose font-mono">
    <h1 class="text-2xl pb-6 font-bold">Blogs</h1>
    <p class="pb-6">This is al list of blog items</p>
    <div class="column text-gray-400 text-sm">
      <div>Date</div>
      <div>Title</div>
    </div>
    <ul>
      <li v-for="post in posts" :key="post._path">
        <NuxtLink :to="post._path" class="column hover:bg-gray-100 dark:hover:bg-gray-800">
          <div :class="{'text-white dark:text-gray-900': !post.displayYear, 'text-gray-400 dark:text-gray-500' :post.displayYear}">{{ post.year}}</div>
          <div>{{ post.title }}</div>
        </NuxtLink>
      </li>
    </ul>
  </section>
</template>

<script setup>
  const { data } = await useAsyncData(
      'blog-list',
      () => queryContent('/blog')
          .where({ _path: { $ne: 'blog' } })
          .only(['_path', 'title', 'publishedAt'])
          .sort({ publishedAt: -1 })
          .find()
  )

  const posts = computed(() => {
    if (!data.value) {
      return []
    }

    const result = []
    let lastYear = null

    for (const post of data.value) {
      const year = new Date(post.publishedAt).getFullYear()
      const displayYear = year !== lastYear
      post.displayYear = displayYear
      post.year = year
      result.push(post)
      lastYear = year
    }

    return result
  })
  console.log(posts)
</script>

<style scoped>
  .column {
    @apply flex items-center space-x-8 py-2 border-b border-gray-200 dark:border-gray-700
  }
</style>