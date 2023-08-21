<template>
  <HeaderComponent />
  <main class="min-h-[700px] bg-[#201F1F] pt-20">
    <slot />
  </main>
  <FooterComponent />
</template>

<script setup></script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Montserrat:wght@400;500;600;700&family=Noto+Sans&display=swap");
@import url("https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css");
</style>
