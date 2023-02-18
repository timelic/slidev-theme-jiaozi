<template>
  <div class="custom-bottom mb-3 mt-auto">
    <slot />
  </div>
</template>

<style>
.custom-bottom + .custom-bottom {
  margin-top: 0;
}
.custom-bottom:not(:last-child) {
  margin-bottom: 0.5rem;
}
</style>
