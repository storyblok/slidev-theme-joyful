<script setup lang="ts">

</script>

<template>
  <aside class="absolute right-0 top-0 h-full flex flex-col justify-between items-center w-16 border-l border-gray-200 py-16">
    <TheIsotype />
    <div class="border-t border-gray-800 px-2 text-[0.65rem] text-gray-800 pt-2">
      {{ $nav.currentPage }}
    </div>
  </aside>
</template>
