<script setup>
const { data } = await useAsyncData('posts', () => queryContent('/').find())

definePageMeta({
  layout: 'home',
})
</script>

<template>
  <div>
    <LatestPost :post="data[0]" />
    <div class="flex-col flex-col items-center gap-3 p-4 py-20 px-10">
      <PostCard v-for="(post, index) in data" :key="post.title" :post="post" :index="index" />
    </div>
  </div>
</template>
