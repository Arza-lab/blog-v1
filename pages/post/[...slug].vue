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

