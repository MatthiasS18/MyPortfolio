<script setup lang="ts">
import ThemeToggle from '@/components/ThemeToggle.vue'
</script>

<template>
  <header class="fixed z-50 w-full">
    <!-- 
      Mode Clair : Fond blanc (bg-white), texte ardoise (text-slate-800), bordure claire
      Mode Sombre : Fond noir ardoise (dark:bg-slate-900), texte blanc (dark:text-white), bordure sombre
    -->
    <nav
      class="bg-white dark:bg-slate-900 text-slate-800 dark:text-white flex items-center justify-between border-b border-slate-200 dark:border-slate-800 px-6 py-4 shadow-lg transition-colors duration-300"
    >
      <a
        href="#home"
        class="text-xl font-bold text-slate-900 dark:text-white transition duration-200 hover:text-blue-500 dark:hover:text-blue-400"
      > 
        Saltan Matthias
      </a>

      <ul class="flex items-center gap-8">
        <li>
          <a
            href="#home"
            class="text-sm font-medium text-slate-600 dark:text-slate-300 transition duration-200 hover:text-blue-500 dark:hover:text-blue-400"
          > 
            Home
          </a>
        </li>

        <li>
          <a
            href="#about"
            class="text-sm font-medium text-slate-600 dark:text-slate-300 transition duration-200 hover:text-blue-500 dark:hover:text-blue-400"
          >
            About
          </a>
        </li>

        <li>
          <a
            href="#skills"
            class="text-sm font-medium text-slate-600 dark:text-slate-300 transition duration-200 hover:text-blue-500 dark:hover:text-blue-400"
          >
            Skills
          </a>
        </li>

        <li>
          <a
            href="#projects"
            class="text-sm font-medium text-slate-600 dark:text-slate-300 transition duration-200 hover:text-blue-500 dark:hover:text-blue-400"
          >
            Projects
          </a>
        </li>

        <li>
          <a
            href="#contact"
            class="text-sm font-medium text-slate-600 dark:text-slate-300 transition duration-200 hover:text-blue-500 dark:hover:text-blue-400"
          >
            Contact
          </a>
        </li>
      </ul>
      
      <ThemeToggle />
    </nav>
  </header>
</template>
