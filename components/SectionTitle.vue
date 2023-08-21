<template>
  <div class="flex items-center justify-between py-5">
    <h2
      class="uppercase font-bold text-2xl md:text-3xl relative flex items-center gap-10"
    >
      <span class="h-[2px] w-14 bg-[#f3c54d]"></span> {{ title }}
    </h2>

    <a
      v-if="text && path"
      class="group sm:flex items-center gap-5 hidden"
      :href="`/${path}`"
    >
      <span class="group-hover:text-[#f3c54d] duration-200">
        {{ text }}
      </span>

      <img src="/icons/arrow-right.svg" alt="➡️" />
    </a>
  </div>
</template>

<script setup>
defineProps(["title", "text", "path"]);
</script>

<style lang="scss" scoped></style>
