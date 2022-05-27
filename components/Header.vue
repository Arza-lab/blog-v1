<script setup>

</script>

<template>
  <header class="mx-auto px-4 sticky top-0 z-50 opacity-90 bg-white backdrop-blur backdrop-filter dark:bg-gray-800">
    <div class="flex justify-between items-center py-6 md:(justify-start)">
      <div class="flex justify-start md:(w-0 flex-1)">
        <a href="/">
          <span class="sr-only">Maurice Schwarz</span>
          <img class="h-10 w-auto sm:h-12" height="100" width="100" src="/logos/M.svg" alt="Maurice Schwarz Logo">
        </a>
      </div>
      <div class="flex items-center justify-end">
        <a class="icon-btn mx-3 dark:text-white" rel="noreferrer" href="https://github.com/Arza-lab" target="_blank" title="GitHub">
          <div class=" i-carbon-logo-github text-xl " />
        </a>
        <DarkToggle />
      </div>
    </div>
  </header>
</template>

<style scoped>

</style>
