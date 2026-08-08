<script setup>
import { ref, onMounted } from 'vue'

const isDark = ref(false)

const toggleTheme = () => {
  isDark.value = !isDark.value
  if (isDark.value) {
    document.documentElement.classList.add('dark')
    localStorage.setItem('theme', 'dark')
  } else {
    document.documentElement.classList.remove('dark')
    localStorage.setItem('theme', 'light')
  }
}

onMounted(() => {
  isDark.value = localStorage.getItem('theme') === 'dark' || 
    (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)
  
  if (isDark.value) document.documentElement.classList.add('dark')
})
</script>

<template>
  <button @click="toggleTheme" class="p-2 rounded cursor-pointer text-slate-800 dark:text-slate-200">
    <span v-if="isDark">☀️</span>
    <span v-else>🌙</span>
  </button>
</template>
