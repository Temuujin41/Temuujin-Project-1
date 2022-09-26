<script setup>
import { ref, computed } from 'vue'
import Home from './components/home/home.vue' 
import HighLights from './components/highlight/HighLights.vue'
import Watch from './components/watch/watch.vue'
import News from './components/news/news.vue'

const routes = {
  '/': Home,
  '/highlight': HighLights,
  '/news': News,
  '/watch': Watch
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/'] || NotFound
})


// Syntax Code's here
</script>

<template>
<div>
  <a href="#/">Home</a> |
  <a href="#/highlight">Highlights</a> |
  <a href="#/watch">Watch</a> |
  <a href="#/news">News</a> |
  <component :is="currentView" />
</div>
</template>

<style >

</style>
