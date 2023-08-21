<template>
  <header class="fixed z-20 top-0 w-full bg-[#151515ee]">
    <Container>
      <nav class="flex items-center justify-between py-[17px]">
        <a href="/" class="flex items-center gap-4 xl:w-min">
          <img src="/icons/logo.svg" alt="logo" />
          <p class="uppercase">
            <span class="font-semibold font-['Inter']">Kyokushinkai </span>
            <span class="font-semibold font-['Inter']">kan</span>
          </p>
        </a>

        <button
          @click="openModal"
          class="block xl:hidden pt-1 px-2 opacity-50 hover:opacity-100 hover:bg-[#161616] rounded"
        >
          <i class="bx bx-menu text-3xl"></i>
        </button>

        <Modal :visible="modalVisible" @close="closeModal">
          <ul class="flex flex-col items-start gap-5 pt-4">
            <li v-for="link in navLinks">
              <router-link
                @click="closeModal"
                class="font-normal hover:text-[#f3c54d] duration-200"
                :to="`/${link.path}`"
              >
                {{ link.text }}
              </router-link>
            </li>
          </ul>
        </Modal>

        <ul class="items-center justify-between gap-9 hidden xl:flex">
          <li v-for="link in navLinks">
            <router-link
              class="font-normal hover:text-[#f3c54d] duration-200"
              :to="`/${link.path}`"
            >
              {{ link.text }}
            </router-link>
          </li>
        </ul>
      </nav>
    </Container>
  </header>
</template>

<script setup>
import { navLinks } from "../../constants/navLinks.js";

const modalVisible = ref(false);

const openModal = () => {
  modalVisible.value = true;
  toggleBodyScroll(false);
};

const closeModal = () => {
  modalVisible.value = false;
  toggleBodyScroll(true);
};

const toggleBodyScroll = (locked) => {
  if (locked) {
    document.body.classList.remove("no-scroll");
  } else {
    document.body.classList.add("no-scroll");
  }
};
</script>

<style lang="scss" scoped>
.router-link-exact-active {
  color: #f3c54d;
}
</style>
