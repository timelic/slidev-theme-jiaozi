<template>
  <template v-if="slidev.nav.currentLayout !== ''">
    <header class="absolute top-6 left-14 flex items-center gap-4 text-sm">
      <span class="flex gap-2">
        <div class="ball bg-red-500" />
        <div class="ball bg-blue-600" />
        <div class="ball bg-black" />
      </span>
    </header>
    <footer class="absolute bottom-6 left-14 right-0 flex gap-4 text-xs">
      This is a title: 2022
    </footer>
  </template>
</template>

<style scoped>
.ball {
  --diameter: 10px;
  width: var(--diameter);
  height: var(--diameter);
  border-radius: 50%;
}
</style>

<script lang="ts" setup>
const slidev = $slidev;
</script>
