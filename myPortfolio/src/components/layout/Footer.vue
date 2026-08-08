<script setup lang="ts">
const links = [
  {
    name: "GitHub",
    url: "https://github.com/MatthiasS18",
  },
  {
    name: "LinkedIn",
    url: "https://linkedin.com/in/matthias-saltan",
  },
]
</script>

<template>
  <!-- 
    bg-white -> dark:bg-slate-900 : Assure que le fond reste raccord avec le reste du site
    border-slate-200 -> dark:border-slate-800 : Ligne de séparation adaptative
    transition-colors duration-300 : Pour le fondu fluide au clic du bouton
  -->
  <footer class="border-t border-slate-200 bg-white px-6 py-8 lg:px-20 dark:border-slate-800 dark:bg-slate-900 transition-colors duration-300">

    <div class="flex flex-col items-center justify-between gap-4 md:flex-row">

      <!-- text-slate-500 -> dark:text-slate-400 -->
      <p class="text-sm text-slate-500 dark:text-slate-400">
        © {{ new Date().getFullYear() }} Matthias. All rights reserved.
      </p>

      <div class="flex gap-6">
        <!-- 
          text-slate-500 -> dark:text-slate-400 : Liens grisés par défaut
          hover:text-indigo-600 -> dark:hover:text-indigo-400 : Effet interactif au survol de la souris
        -->
        <a
          v-for="link in links"
          :key="link.name"
          :href="link.url"
          target="_blank"
          class="text-sm text-slate-500 transition-colors duration-200 hover:text-indigo-600 dark:text-slate-400 dark:hover:text-indigo-400"
        >
          {{ link.name }}
        </a>
      </div>

    </div>

  </footer>
</template>

<style scoped>
</style>
