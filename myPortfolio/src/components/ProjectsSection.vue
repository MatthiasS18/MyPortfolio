<script setup lang="ts">
const projects = [
  {
    title: "BudgetMate",
    description:
      "A mobile application that helps users manage their personal finances by tracking expenses, incomes, and budgets. Includes authentication, premium features, and AI-powered financial analysis.",
    technologies: [
      "Kotlin",
      "Jetpack Compose",
      "Firebase",
      "Room",
      "Gemini API",
    ],
    github: "#",
    demo: "#",
    inWorking: true
  },
  {
    title: "Recipe App",
    description:
      "A web application for managing recipes with CRUD operations, data persistence, and a clean user interface.",
    technologies: [
      "Laravel",
      "MySQL",
      "PHP",
    ],
    github: "#",
    demo: "#",
    inWorking: false
  },
]
</script>

<template>
  <!-- 
    bg-white -> dark:bg-slate-900 : Gestion du fond de la section principale
    transition-colors duration-300 : Assure le fondu fluide lors du changement de mode
  -->
  <section id="projects" class="px-6 py-24 lg:px-20 bg-white dark:bg-slate-900 transition-colors duration-300">

    <p class="mb-2 text-sm font-semibold uppercase tracking-[0.3em] text-indigo-600 dark:text-indigo-400">
      My work
    </p>

    <!-- text-slate-900 -> dark:text-white -->
    <h2 class="text-4xl font-bold text-slate-900 dark:text-white">
      Projects
    </h2>

    <!-- text-slate-600 -> dark:text-slate-400 -->
    <p class="mt-4 max-w-2xl text-slate-600 dark:text-slate-400">
      Here are some of the projects I have developed to improve my skills and
      create real-world applications.
    </p>

    <div class="mt-12 grid gap-8 md:grid-cols-2 xl:grid-cols-3">
      <article
        v-for="project in projects"
        :key="project.title"
        class="overflow-hidden rounded-xl border border-slate-200 bg-slate-50 dark:border-slate-800 dark:bg-slate-900/40"
      >
        <!-- Working banner -->
        <div
          v-if="project.inWorking"
          class="bg-red-600 px-4 py-2 text-center text-sm font-semibold text-white"
        >
          Still working on it
        </div>

        <!-- Image placeholder : bg-slate-200 (clair) -> dark:bg-slate-800 (sombre) -->
        <div class="flex h-48 items-center justify-center bg-slate-200 dark:bg-slate-800">
          <span class="text-slate-500 dark:text-slate-400">
            Project Image
          </span>
        </div>

        <div class="p-6">
          <!-- text-slate-900 -> dark:text-white -->
          <h3 class="text-xl font-semibold text-slate-900 dark:text-white">
            {{ project.title }}
          </h3>

          <!-- text-slate-600 -> dark:text-slate-400 -->
          <p class="mt-3 text-sm leading-6 text-slate-600 dark:text-slate-400">
            {{ project.description }}
          </p>

          <!-- Badges de technologies -->
          <div class="mt-4 flex flex-wrap gap-2">
            <!-- 
              Mode clair : texte indigo contrasté sur fond violet léger 
              Mode sombre : texte lumineux sur fond transparent
            -->
            <span
              v-for="technology in project.technologies"
              :key="technology"
              class="rounded-full bg-indigo-50 dark:bg-indigo-50/10 px-3 py-1 text-xs font-medium text-indigo-600 dark:text-indigo-300"
            >
              {{ technology }}
            </span>
          </div>

          <!-- Liens de bas de carte -->
          <!-- <div class="mt-6 flex gap-4">
            <a
              :href="project.github"
              class="text-sm font-semibold text-indigo-600 hover:text-indigo-500 dark:text-indigo-400 dark:hover:text-indigo-300"
            >
              GitHub
            </a>

            <a
              :href="project.demo"
              class="text-sm font-semibold text-indigo-600 hover:text-indigo-500 dark:text-indigo-400 dark:hover:text-indigo-300"
            >
              Demo
            </a>
          </div> -->
        </div>
      </article>
    </div>

  </section>
</template>

<style scoped>
</style>
