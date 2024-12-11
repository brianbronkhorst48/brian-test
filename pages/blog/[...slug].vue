<template>
  <article class="prose dark:prose-invert prose-pre:bg-white dark:prose-pre:bg-gray-800 prose-pre:text-gray-700 dark:prose-pre:text-gray-300">
    <ContentDoc>
      <template #not-found>
        <h1>Page not found (404)</h1>
        <p>This blog page can not be found</p>
      </template>
      <template v-slot=" {doc} ">
        <div class="grid grid-cols-6 gap-16">
          <div class="col-span-4">
            <ContentRenderer :value="doc" />
          </div>
          <div class="col-span-2" >
          <aside class="sticky top-8">
            <div class="font-semibold mb-2">
              Table of contents
            </div>
            <nav>
              <TocLinks :links="doc.body.toc.links"/>
            </nav>
          </aside>
          </div>
        </div>
      </template>
    </ContentDoc>
  </article>
</template>

<script setup>
const route = useRoute();
console.log(route);
</script>