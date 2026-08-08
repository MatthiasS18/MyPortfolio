<script setup lang="ts">
</script>

<template>
  <!-- 
    bg-white -> dark:bg-slate-900 : Gestion du fond de la section principale
    transition-colors duration-300 : Assure le fondu fluide lors du clic sur le bouton
  -->
  <section
    id="home"
    class="flex min-h-screen flex-col justify-center px-6 lg:px-20 bg-white dark:bg-slate-900 transition-colors duration-300"
  >
    <!-- text-indigo-600 s'adapte en text-indigo-400 sur fond sombre -->
    <p class="mb-4 text-sm font-semibold uppercase tracking-[0.3em] text-indigo-600 dark:text-indigo-400">
      👋 Welcome to my portfolio
    </p>

    <!-- text-slate-900 -> dark:text-white -->
    <h1 class="text-5xl font-extrabold text-slate-900 dark:text-white md:text-7xl">
      Hi, I'm <span class="text-indigo-600 dark:text-indigo-400">Matthias</span>
    </h1>

    <!-- text-slate-700 -> dark:text-slate-300 -->
    <h2 class="mt-4 text-2xl font-semibold text-slate-700 dark:text-slate-300 md:text-3xl">
      Full-Stack & Mobile Application Developer
    </h2>

    <!-- text-slate-600 -> dark:text-slate-400 -->
    <p class="mt-8 max-w-2xl text-lg leading-8 text-slate-600 dark:text-slate-400">
      I build modern web and mobile applications with a focus on clean code,
      performance, and user experience. I enjoy learning new technologies and
      creating solutions that solve real-world problems.
    </p>

    <!-- Boutons d'action -->
    <div class="mt-10 flex flex-wrap gap-4">
      <a
        href="#projects"
        class="rounded-lg bg-indigo-600 px-6 py-3 font-semibold text-white transition-colors duration-200 hover:bg-indigo-700 dark:bg-indigo-600 dark:hover:bg-indigo-500"
      >
        View Projects
      </a>

      <!-- 
        Mode Clair : Bordure grise (border-slate-300) et texte sombre (text-slate-700)
        Mode Sombre : Bordure et texte clairs (dark:border-slate-600 dark:text-white)
      -->
      <a
        href="../assets/cv/Lettre_de_motivation-Matthias_Saltan.pdf"
        download="CV-Matthias_Saltan.pdf"
        target="_blank"
       class="rounded-lg bg-indigo-600 px-6 py-3 font-semibold text-white transition-colors duration-200 hover:bg-indigo-700 dark:bg-indigo-600 dark:hover:bg-indigo-500"
      >
        Download CV
      </a>

    </div>
  </section>
</template>
