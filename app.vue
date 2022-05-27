<script setup>
useHead({
  title: 'Blog Maurice Schwarz | Web Entwickler',
  viewport: 'width=device-width, initial-scale=1, maximum-scale=1',
  charset: 'utf-8',
  meta: [
    { name: 'description', content: 'Maurice Schwarz ist Software Entwickler, darauf spezialisiert, außergewöhnliche digitale Erlebnisse zu entwerfen und umzusetzen.' },
  ],
  link: [
    {
      rel: 'icon', type: 'image/svg', href: 'logos/M.svg',
    },
  ],
})
</script>

<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<style>
html, body , #__nuxt{
  height: 100vh;
  margin: 0;
  padding: 0;
}

html.light {
  background: #f3f4f6;
}

html.dark {
  background: #121212;
  color: white;
}
</style>
