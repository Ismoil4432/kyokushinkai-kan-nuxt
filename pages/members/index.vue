<template>
  <section id="members">
    <Container>
      <div class="min-h-[700px] pt-20">
        <PageTitle :title="title" />
      </div>
    </Container>
  </section>
</template>

<script setup>
const title = "Barcha murabbiylar";

useHead({
  title,
});
</script>

<style lang="scss" scoped></style>
