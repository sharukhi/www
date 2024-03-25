<template>
  <div class="space-y-6">
    <NuxtImg src="/avatar.jpeg" alt="Sharukhi"
      class="ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 bg-gray-200 dark:bg-gray-900 rounded-full h-12 w-12 sm:h-16 sm:w-16"
      sizes="48px sm:64px" placeholder format="webp" />
    <h1 class="text-xl font-bold tracking-tight text-gray-800 dark:text-gray-100">
      Hello!
    </h1>
    <p class="text-gray-900 dark:text-gray-400">
      I'm Ataullah Sharukhi, an indie developer based in Bangladesh. I specialize in building web applications and sites
      using using Javascript, Svelte & Flask . I am always up for a challenge and eager to learn and grow. I am also
      excited about where my love for technology will take me in the future!
    </p>
  </div>
</template>

<script setup>
useSeoMeta({
  title: "Sharukhi",
  description:
    "I'm Ataullah Sharukhi, an indie developer based in Bangladesh. You can find more about me...",
});
</script>
