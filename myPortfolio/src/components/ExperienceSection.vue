<script setup lang="ts">
const experiences = [
  {
    period: "2025",
    title: "Bachelor in Application Development",
    company: "HE2B ESI",
    description:
      "Graduated with a bachelor's degree in Application Development, working on web, mobile, and backend projects.",
  },
  {
    period: "2025 - Present",
    title: "Personal Projects",
    company: "Self-learning",
    description:
      "Developing modern web and mobile applications to strengthen my skills in Vue.js, Kotlin, Firebase, and Spring Boot.",
  },
]
</script>

<template>
  <!-- 
    bg-white -> dark:bg-slate-900 : Changement automatique du fond de la section
    transition-colors duration-300 : Assure le basculement fluide
  -->
  <section id="about" class="px-6 py-24 lg:px-20 bg-white dark:bg-slate-900 transition-colors duration-300">
    
    <!-- text-indigo-600 s'adapte en text-indigo-400 en mode sombre pour rester lumineux -->
    <p class="mb-2 text-sm font-semibold uppercase tracking-[0.3em] text-indigo-600 dark:text-indigo-400">
      My Journey
    </p>

    <!-- text-slate-900 -> dark:text-white -->
    <h2 class="text-4xl font-bold text-slate-900 dark:text-white">
      Experience & Education
    </h2>

    <!-- text-slate-600 -> dark:text-slate-400 -->
    <p class="mt-4 max-w-2xl text-slate-600 dark:text-slate-400">
      My academic background and personal projects have allowed me to build
      practical experience across web, mobile, and backend development.
    </p>

    <!-- Liste des blocs d'expérience -->
    <div class="mt-12 space-y-8">
      <div
        v-for="experience in experiences"
        :key="experience.title"
        class="rounded-xl border border-slate-200 bg-slate-50 p-6 dark:border-slate-800 dark:bg-slate-900/40"
      >
        <p class="text-sm font-semibold text-indigo-600 dark:text-indigo-400">
          {{ experience.period }}
        </p>

        <h3 class="mt-2 text-xl font-semibold text-slate-900 dark:text-white">
          {{ experience.title }}
        </h3>

        <p class="text-slate-700 dark:text-slate-300 font-medium">
          {{ experience.company }}
        </p>

        <p class="mt-4 leading-7 text-slate-600 dark:text-slate-400">
          {{ experience.description }}
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
