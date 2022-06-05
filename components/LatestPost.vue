<script setup>
defineProps({
  post: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div v-motion-fade class="flex flex-col items-center">
    <div>
      <img src="https://picsum.photos/1920/400" alt="" class="p-0 m-0 object-contain">
    </div>
    <div class="p-4 gap-3 transition ease-in-out w-2/3  bg-white flex -mt-25 flex-col items-center dark:bg-gray-800">
      <h1 class="font-serif text-4xl rainbow-text">
        {{ post.title }}
      </h1>
      <p class="">
        {{ post.description }}
      </p>
      <div class="grid grid-cols-12 gap-3">
        <div class="font-normal flex flex-col col-span-12 md:col-span-6 opacity-75">
          <p>
            {{ post.date }}
          </p>
          <p class="">
            {{ post.timeToRead }}
          </p>
        </div>
        <NuxtLink :to="post._path" class="btn col-span-12 md:col-span-6">
          Mehr erfahren
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
