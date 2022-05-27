<script setup>
const { data } = await useAsyncData('home', () => queryContent('/').find())
console.log(data)
</script>

<template>
  <div>
    <Logos mb-6 />
    <Suspense>
      <div class="flex-col flex-col items-center gap-3 p-4">
        <PostCard v-for="post in data" :key="post.title" :post="post" />
      </div>
      <template #fallback>
        <div op50 italic>
          <span animate-pulse>Loading...</span>
        </div>
      </template>
    </Suspense>
  </div>
</template>
