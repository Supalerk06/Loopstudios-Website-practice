<script setup>
import { ref } from 'vue';

defineProps({
  menuItems: {
    type: Array,
    required: true,
  },
});

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
  <section
    class="relative bg-[url('assets/mobile/image-hero.jpg')] bg-no-repeat bg-cover bg-center md:bg-[url('assets/desktop/image-hero.jpg')]"
  >
    
    <div
      v-if="isMenuOpen"
      class="absolute inset-0 z-20 bg-black md:hidden"
    ></div>

    <div class="container relative z-30 mx-auto max-w-6xl px-6 py-12">
      <nav class="flex items-center justify-between font-bold text-white">
        <img src="../assets/logo.svg" alt="Loopstudios Logo" />
        
        
        <div class="hidden h-10 font-sans md:flex md:space-x-8">
          <div v-for="item in menuItems" :key="item.name" class="group">
            <a :href="item.link">{{ item.name }}</a>
            <div
              class="mx-2 group-hover:border-b group-hover:border-blue-50"
            ></div>
          </div>
        </div>

        
        <button class="md:hidden" @click="toggleMenu">
          <img v-if="!isMenuOpen" src="../assets/icon-hamburger.svg" alt="Open Menu" />
          <img v-else src="../assets/icon-close.svg" alt="Close Menu" />
        </button>
      </nav>

      
      <div v-if="isMenuOpen" class="md:hidden mt-32 flex flex-col space-y-6 font-sans text-2xl uppercase text-white font-light">
        <div v-for="item in menuItems" :key="item.name + '-mobile'" class="group w-fit">
          <a :href="item.link">{{ item.name }}</a>
          <div class="mx-2 group-hover:border-b group-hover:border-blue-50"></div>
        </div>
      </div>

      
      <div v-if="!isMenuOpen" class="max-w-xl p-6 mt-32 mb-10 border-2 border-white font-sans md:p-10 md:mt-32">
        <h1 class="text-4xl text-white uppercase md:text-6xl">
          Immersive experiences that deliver
        </h1>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>