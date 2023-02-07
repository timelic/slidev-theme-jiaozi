<template>
  <div class="slidev-layout">
    <div class="my-auto w-full">
      <header>
        <!-- <div>{{ header }}test</div> -->
      </header>
      <slot />
      <footer></footer>
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps<{
  header: string;
}>();
</script>
