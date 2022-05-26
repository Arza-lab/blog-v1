<script setup>
const { data } = await useAsyncData('home', () => queryContent('/').find())
</script>

<template>
  <div>
    <Logos mb-6 />
    <Suspense>
      <div class="flex flex-col gap-4 items-center">
        <NuxtLink
          v-for="post in data" :key="post.title" :to="post._path"
          class="mb-4 rounded-md transition ease-in-out h-30 w-3/4 bg-gray-100 border-md shadow-md flex items-left text-left justify-left hover:(text-teal-800 shadow-lg)"
        >
          <h2 class="font-serif text-2xl text-teal-600 hover:(text-teal-800)  p-4">
            {{ post.title }}
          </h2>
        </NuxtLink>
      </div>
      <template #fallback>
        <div op50 italic>
          <span animate-pulse>Loading...</span>
        </div>
      </template>
    </Suspense>
  </div>
</template>
