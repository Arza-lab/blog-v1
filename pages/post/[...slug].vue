<script setup>
const router = useRouter()
</script>

<template>
  <main>
    <ContentDoc />
    <div>
      <button btn text-sm m="3 t8" @click="router.back()">
        cd ..
      </button>
    </div>
  </main>
</template>

<style>
h1 {
  @apply text-teal-600 text-5xl;
  font-size: 2.5rem!important;
  margin-bottom: 2rem;
}
</style>
