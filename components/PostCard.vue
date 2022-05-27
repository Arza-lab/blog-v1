<script setup>
defineProps({
  post: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div class="grid grid-cols-1 md:(grid-cols-3) content-center shadow-sm mb-4 rounded-md">
    <div class="w-full items-right col-span-1 flex flex-col">
      <img src="https://picsum.photos/370/240" :alt="post.title">
    </div>
    <NuxtLink
      :to="post._path"
      class="p-4 col-span-2  transition ease-in-out w-full bg-white  flex flex-col items-left text-left justify-left hover:(text-teal-800)"
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
</template>
