<script setup>
defineProps({
  post: {
    type: Object,
    required: true,
  },
  index: {
    type: Number,
    required: true,
  },
})
</script>

<template>
  <div v-if="index !== 0" v-motion-fade  class="grid grid-cols-12 content-center shadow-sm mb-4 rounded-lg dark:bg-gray-900 bg-transparent">
    <div class="w-full items-right col-span-12 flex flex-col md:(col-span-4)">
      <img src="https://picsum.photos/370/240" :alt="post.title">
    </div>
    <NuxtLink
      :to="post._path"
      class="p-4 col-span-12 transition ease-in-out w-full bg-white  flex flex-col items-left text-left justify-left md:(col-span-8) hover:(text-teal-600) dark:bg-gray-800"
    >
      <h2 class="font-serif text-3xl text-teal-600">
        {{ post.title }}
      </h2>
      <p class="test-xl">
        {{ post.description }}
      </p>
      <div class="text-lg flex flex-col">
        <p>
          {{ post.date }}
        </p>
        <p class="opacity-75">
          {{ post.timeToRead }}
        </p>
      </div>
    </NuxtLink>
  </div>
</template>
