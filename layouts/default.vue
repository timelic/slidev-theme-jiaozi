<template>
  <div class="slidev-layout">
    <div class="w-full">
      <slot />
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps<{
  header: string;
}>();
</script>
