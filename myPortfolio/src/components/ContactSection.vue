<script setup lang="ts">
const contacts = [
  {
    name: "Email",
    value: "matthiassaltan71@gmail.com",
    link: "mailto:matthiassaltan71@gmail.com",
  },
  {
    name: "GitHub",
    value: "https://github.com/MatthiasS18",
    link: "https://github.com/MatthiasS18",
  },
  {
    name: "LinkedIn",
    value: "www.linkedin.com/in/matthias-saltan",
    link: "www.linkedin.com/in/matthias-saltan",
  },
]
</script>

<template>
  <!-- 
    bg-white -> dark:bg-slate-900 : Changement global du fond de la section
    transition-colors duration-300 : Pour un basculement fluide
  -->
  <section id="contact" class="px-6 py-24 lg:px-20 bg-white dark:bg-slate-900 transition-colors duration-300">

    <!-- text-indigo-600 s'adapte en text-indigo-400 sur fond sombre pour un meilleur contraste -->
    <p class="mb-2 text-sm font-semibold uppercase tracking-[0.3em] text-indigo-600 dark:text-indigo-400">
      Get in touch
    </p>

    <!-- text-slate-900 (clair) -> dark:text-white (sombre) -->
    <h2 class="text-4xl font-bold text-slate-900 dark:text-white">
      Contact
    </h2>

    <!-- text-slate-600 (clair) -> dark:text-slate-400 (sombre) -->
    <p class="mt-4 max-w-2xl text-slate-600 dark:text-slate-400">
      I'm always open to discussing new opportunities, projects, or simply
      exchanging ideas about software development.
    </p>

    <!-- Grille des cartes de contact -->
    <div class="mt-10 grid gap-6 md:grid-cols-3">
      <a
        v-for="contact in contacts"
        :key="contact.name"
        :href="contact.link"
        target="_blank"
        class="rounded-xl border border-slate-200 bg-slate-50 p-6 transition-all duration-200 hover:border-indigo-500 dark:border-slate-800 dark:bg-slate-900/40 dark:hover:border-indigo-500"
      >
        <h3 class="text-lg font-semibold text-slate-900 dark:text-white">
          {{ contact.name }}
        </h3>

        <p class="mt-2 text-slate-600 dark:text-slate-400 break-all">
          {{ contact.value }}
        </p>
      </a>
    </div>

    <!-- Bloc d'appel à l'action final -->
    <div class="mt-12 rounded-xl border border-slate-200 bg-slate-50 p-8 dark:border-slate-800 dark:bg-slate-900/40">
      <h3 class="text-2xl font-semibold text-slate-900 dark:text-white">
        Let's work together
      </h3>

      <p class="mt-3 max-w-xl text-slate-600 dark:text-slate-400">
        If you have an opportunity or a project in mind, feel free to reach out.
        I would be happy to discuss how I can contribute.
      </p>

      <a
        href="mailto:matthias@email.com"
        class="mt-6 inline-block rounded-lg bg-indigo-600 px-6 py-3 font-semibold text-white transition-colors duration-200 hover:bg-indigo-700 dark:bg-indigo-600 dark:hover:bg-indigo-500"
      >
        Send me an email
      </a>
    </div>

  </section>
</template>

<style scoped>
</style>
