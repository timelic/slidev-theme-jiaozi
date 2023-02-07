<template>
  <div class="slidev-layout">
    <div class="my-auto h-full w-full flex">
      <div
        class="left flex-shrink-0"
        :style="{ width: `calc(${textScale} * 100%)`, order: leftOrder }"
      >
        <slot />
      </div>
      <div
        class="right flex-shrink-0 flex flex-col gap-4"
        :style="{ width: `calc(${textScale} * 100%)`, order: rightOrder }"
      >
        <div class="relative flex-1 w-full flex justify-center items-center">
          <img
            class="rounded-md absolute max-h-full object-contain"
            :src="img"
          />
        </div>
        <div v-if="caption" class="text-center">{{ caption }}</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { withDefaults, computed } from "vue";
const { textPos } = withDefaults(
  defineProps<{
    img: string;
    caption: string;
    textPos: "left" | "right";
    textScale: number;
  }>(),
  {
    textPos: "left",
    textScale: 0.65,
  }
);
const leftOrder = computed(() => (textPos === "left" ? 1 : 2));
const rightOrder = computed(() => (textPos === "left" ? 2 : 1));
</script>
