<script lang="ts" setup>
import Bottom from "./Bottom.vue";
defineProps<{
  href?: string;
}>();
</script>

<template>
  <Bottom>
    <ul class="text-sm text-gray-500">
      <template v-if="href">
        <li>
          <a :href="href" target="_blank" rel="noopener noreferrer">
            <slot />
          </a>
        </li>
      </template>
      <template v-else>
        <li><slot /></li>
      </template>
    </ul>
  </Bottom>
</template>

<style scoped>
li {
  line-height: unset !important;
}
</style>
