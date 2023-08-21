<template>
  <section id="hall">
    <Container>
      <div class="min-h-[700px] pt-20">
        <PageTitle :title="title" />
      </div>
    </Container>
  </section>
</template>

<script setup>
const title = "Sport zallar";

useHead({
  title,
});
</script>

<style lang="scss" scoped></style>
