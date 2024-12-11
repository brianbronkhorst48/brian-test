<template>
  <NuxtLayout>
    <section class="">
      <h1 class="text-4xl"> Opss.... {{ error.statusCode }}</h1>
      <p class="text-xl mt-4">{{ error.statusMessage }}</p>
    </section>
  </NuxtLayout>
</template>
<script setup>
defineProps({error: Object })
</script>