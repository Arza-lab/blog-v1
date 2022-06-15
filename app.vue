<script setup>
useHead({
  htmlAttrs: {
    lang: 'de',
  },
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
.rainbow-text {
	@apply text-transparent bg-clip-text bg-gradient-to-r from-emerald-500 via-teal-600 to-teal-700;
}
.page-enter-active,
.page-leave-active {
	transition: all 0.3s ease-in-out;
}

.page-enter-from,
.page-leave-to {
	opacity: 0;
	transform: scale(0.99);
}
</style>
