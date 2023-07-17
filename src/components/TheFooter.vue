<template>
  <nav mt-6 inline-flex gap-2 text-xl>
    <button icon-btn @click="toggleDark()">
      <div i-carbon-sun dark:i-carbon-moon data-cursor="block" />
    </button>

    <a

      rel="noreferrer"
      href="https://github.com/antfu/vitesse-lite"
      target="_blank"
      title="GitHub"
      data-cursor="block"
      i-carbon-logo-github cursor-none icon-btn
    />
  </nav>
</template>
