<template>
  <section id="intro" class="relative min-h-[700px]">
    <video
      v-if="mounted"
      loop
      muted
      playsinline
      ref="video"
      class="absolute top-0 left-0 w-full h-full object-cover z-0"
    >
      <source src="/video.mp4" type="video/mp4" />
    </video>

    <div class="relative z-10 bg-black bg-opacity-40">
      <Container>
        <div
          class="flex flex-col lg:flex-row items-center justify-center lg:justify-between gap-8 sm:gap-10 min-h-[700px] pb-20"
        >
          <div class="flex flex-col gap-3 sm:gap-5 text-center lg:text-start">
            <h1 class="text-3xl sm:text-5xl md:text-6xl lg:text-7xl">
              KYOKUSHINKAI-KAN
            </h1>
            <h2 class="text-xl sm:text-3xl md:text-4xl lg:text-5xl opacity-70">
              KARATE UZBEKISTAN
            </h2>
          </div>

          <button @click="video.paused ? video.play() : video.pause()">
            <img src="/icons/play-video.svg" alt="play" />
          </button>
        </div>
      </Container>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from "vue";

const video = ref(null);
const mounted = ref(false);

onMounted(() => {
  mounted.value = true;
});
</script>

<style scoped></style>
