<script setup>
const router = useRouter()
</script>

<template>
  <article>
    <ContentDoc class="prose" />
    <div>
      <button btn text-sm m="3 t8" @click="router.back()">
        cd ..
      </button>
    </div>
  </article>
</template>

<style>
prose h1 {
  @apply text-teal-600 text-4xl mb-3;
}
</style>
