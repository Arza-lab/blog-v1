<script setup>
const { data } = await useAsyncData('home', () => queryContent('/').find())
console.log(data)
</script>

<template>
  <div>
    <Logos mb-6 />
    <Suspense>
      <div class="flex flex-col gap-4 items-center">
        <NuxtLink
          v-for="post in data" :key="post.title" :to="post._path"
          class="p-4 mb-4 rounded-md transition ease-in-out h-30 w-3/4 bg-gray-100 border-md shadow-md flex flex-col items-left text-left justify-left hover:(text-teal-800 shadow-lg)"
        >
          <h2 class="font-serif text-2xl text-teal-600 hover:(text-teal-800)">
            {{ post.title }}
          </h2>
          <div>
            <p class="text-sm flex">
              {{ post.date }}
            </p>
            <p>
              {{ post.timeToRead }}
            </p>
          </div>
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
