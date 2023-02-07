<template>
  <div class="slidev-layout">
    <div class="my-auto w-full">
      <slot />
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps<{
  header: string;
}>();
</script>
