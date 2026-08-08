<script setup lang="ts">
// Ready for your future TypeScript logic
</script>

<template>
  <!-- 
    min-h-screen: so the section takes the full screen height
    bg-white -> dark:bg-slate-900: the background changes automatically
    text-slate-900 -> dark:text-white: the text changes automatically
  -->
  <section 
    id="about" 
    class="min-h-screen bg-white dark:bg-slate-900 text-slate-900 dark:text-white p-8 md:p-16 flex flex-col justify-center transition-colors duration-300"
  >
    <!-- The title adapts automatically, we add a subtle bottom border -->
    <h2 class="text-3xl font-bold mb-4 border-b border-slate-200 dark:border-slate-800 pb-2">
      About Me
    </h2>
    
    <p class="text-slate-600 dark:text-slate-300 max-w-2xl leading-relaxed">
      Passionate developer focused on building modern, high-performance web applications. 
      This is the perfect place to introduce yourself, your journey, and your goals.
    </p>
  </section>
</template>

<style scoped>
/* No CSS needed here, Tailwind handles everything! */
</style>
