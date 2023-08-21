<template>
  <section id="about">
    <Container>
      <div class="min-h-[700px] pt-20">
        <PageTitle :title="title" />
      </div>
    </Container>
  </section>
</template>

<script setup>
const title = "Biz haqimizda";

useHead({
  title,
});
</script>

<style lang="scss" scoped></style>
