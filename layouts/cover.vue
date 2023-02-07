<script setup lang="ts">
defineProps({
  title: {
    type: String,
    default: '文章标题',
  },
  subtitle: {
    type: String,
    default: 'A presentation framework for Vue 3',
  },
  latinDecoration: {
    type: String,
    default: 'PAPERHERE',
  },
})
</script>

<template>
  <div
    class="slidev-layout cover"
  >
    <div class="my-auto w-full">
      <img src="/cover.jpg" class="absolute h-full right-0 top-0 scale-110">
      <div class="main">
        <div class="title text-6xl mb-2">{{ title }}</div>
        <div class="flex items-center">
          <div class="h-11 flex mr-4 ml-1">
            <div class="bg-blue-600 w-7 h-full"/>
            <div class="bg-blue-400 w-7 h-full"/>
            <div class="bg-blue-200 w-7 h-full"/>
          </div>
          <div class="decoration text-6xl font-extrabold">{{ latinDecoration }}</div>
        </div>
        <div class="subtitle mt-2 text-sm">{{ subtitle }}</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.title {
  font-family: 'Kanit', Pingfang, sans-serif;
  font-weight: bolder;
  color: rgb(27, 27, 191);
  font-weight: 900;
}
.decoration {
  font-family: 'Kanit', sans-serif;
  font-style: italic;
  -webkit-text-stroke: 2px rgb(27, 27, 191);
  color: transparent
}
.subtitle {
  font-family: 'Kanit', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
</style>
