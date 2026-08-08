<script setup lang="ts">
const skillCategories = [
  {
    title: "Frontend",
    skills: [
      "Vue.js",
      "React",
      "Angular",
      "TypeScript",
      "JavaScript",
      "HTML5",
      "CSS3",
      "Tailwind CSS",
    ],
  },
  {
    title: "Backend",
    skills: [
      "Node.js",
      "Express",
      "Spring Boot",
      "Laravel",
      "REST API",
    ],
  },
  {
    title: "Mobile",
    skills: [
      "Kotlin",
      "Jetpack Compose",
      "Android",
      "Firebase",
      "Room",
    ],
  },
  {
    title: "Databases",
    skills: [
      "MySQL",
      "PostgreSQL",
      "Firebase Firestore",
    ],
  },
  {
    title: "Tools",
    skills: [
      "Git",
      "GitHub",
      "Docker",
      "Postman",
      "Android Studio",
      "Visual Studio Code",
      "IntelliJ IDEA",
    ],
  },
]
</script>

<template>
  <!-- 
    bg-white -> dark:bg-slate-900 : Gestion du fond de la section principale
    transition-colors duration-300 : Assure une transition de couleur fluide
  -->
  <section id="skills" class="px-6 py-24 lg:px-20 bg-white dark:bg-slate-900 transition-colors duration-300">
    
    <p class="mb-2 text-sm font-semibold uppercase tracking-[0.3em] text-indigo-600 dark:text-indigo-400">
      What I work with
    </p>

    <!-- text-slate-900 -> dark:text-white -->
    <h2 class="text-4xl font-bold text-slate-900 dark:text-white">
      Skills & Technologies
    </h2>

    <!-- text-slate-600 -> dark:text-slate-400 -->
    <p class="mt-4 max-w-2xl text-slate-600 dark:text-slate-400">
      Here are the technologies and tools I use to build modern web and mobile applications.
    </p>

    <!-- Grille des catégories de compétences -->
    <div class="mt-12 grid gap-6 md:grid-cols-2 xl:grid-cols-3">
      <div
        v-for="category in skillCategories"
        :key="category.title"
        class="rounded-xl border border-slate-200 bg-slate-50 p-6 dark:border-slate-800 dark:bg-slate-900/40"
      >
        <!-- text-slate-900 -> dark:text-white -->
        <h3 class="mb-4 text-xl font-semibold text-slate-900 dark:text-white">
          {{ category.title }}
        </h3>

        <div class="flex flex-wrap gap-2">
          <!-- 
            Mode clair : texte indigo contrasté sur fond violet léger (bg-indigo-50 text-indigo-600)
            Mode sombre : texte lumineux sur fond transparent (dark:bg-indigo-50/10 dark:text-indigo-300)
          -->
          <span
            v-for="skill in category.skills"
            :key="skill"
            class="rounded-full bg-indigo-50 dark:bg-indigo-50/10 px-3 py-1 text-sm font-medium text-indigo-600 dark:text-indigo-300"
          >
            {{ skill }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
