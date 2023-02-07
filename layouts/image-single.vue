<template>
  <div class="slidev-layout">
    <div class="my-auto h-full w-full p-8 flex flex-col gap-4 items-center">
      <div class="relative flex-1 w-full flex justify-center">
        <img
          class="rounded-md absolute h-full z-10"
          :src="img"
        />
      </div>
      <div v-if="caption">{{ caption }}</div>
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps<{
  img: string;
  caption: string;
}>();
</script>
