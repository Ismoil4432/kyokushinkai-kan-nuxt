<template>
  <div class="flex items-center justify-between py-5">
    <h2
      class="uppercase font-bold text-2xl md:text-3xl relative flex items-center gap-10"
    >
      <span class="h-[2px] w-10 md:w-20 bg-[#f3c54d]"></span> {{ title }}
    </h2>
  </div>
</template>

<script setup>
defineProps(["title"]);
</script>

<style lang="scss" scoped></style>
