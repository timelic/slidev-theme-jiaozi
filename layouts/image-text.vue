<template>
  <div class="slidev-layout">
    <div class="my-auto h-full w-full flex gap-8">
      <div
        class="left flex-shrink-0"
        :style="{ flexGrow: textScale, order: leftOrder, flexBasis: 0 }"
      >
        <slot />
      </div>
      <div
        class="right flex-shrink-0 flex flex-col gap-4 justify-center items-center"
        :style="{ flexGrow: 1 - textScale, order: rightOrder, flexBasis: 0 }"
      >
        <img
            class="rounded-md max-h-full object-contain overflow-hidden"
            :src="img"
            style="width: fit-content"
          />
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
