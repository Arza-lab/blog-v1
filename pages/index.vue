<script setup>
const { data } = await useAsyncData('posts', () => queryContent('/').find())

definePageMeta({
  layout: 'home',
})
</script>

<template>
  <div>
    <div class="flex flex-col items-center">
      <div>
        <img src="https://picsum.photos/1920/400" alt="" class="p-0 m-0 object-contain">
      </div>
      <div class="p-4 gap-3 transition ease-in-out w-2/3  bg-white flex -mt-25 flex-col items-center hover:(text-teal-600) dark:bg-gray-800">
        <h1 class="font-serif text-4xl text-teal-600">
          {{ data[0].title }}
        </h1>
        <p class="">
          {{ data[0].description }}
        </p>
        <div class="font-normal flex flex-col gap-3">
          <p>
            {{ data[0].date }}
          </p>
          <p class="">
            {{ data[0].timeToRead }}
          </p>
        </div>
        <NuxtLink to="" class="btn">
          Lies weiter
        </NuxtLink>
      </div>
    </div>
    <Suspense>
      <div class="flex-col flex-col items-center gap-3 p-4 py-20 px-10">
        <PostCard v-for="(post, index) in data" :key="post.title" :post="post" :index="index" />
      </div>
      <template #fallback>
        <div op50 italic>
          <span animate-pulse>Loading...</span>
        </div>
      </template>
    </Suspense>
  </div>
</template>
