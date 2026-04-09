<script setup>
defineProps({
  menuItems: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <footer class="bg-black py-10">
    <div class="container mx-auto px-6 max-w-6xl md:px-0 flex flex-col items-center md:flex-row md:justify-between space-y-12 md:space-y-0">
      
      
      <div class="flex flex-col items-center space-y-8 md:space-y-6 md:items-start">
        <img src="../assets/logo.svg" alt="Loopstudios Logo" class="w-36" />
        <div class="flex flex-col gap-3 space-y-4 text-center text-white font-bold font-sans md:flex-row md:space-y-0 md:space-x-8 md:text-left">
          <div v-for="item in menuItems" :key="item.name" class="group mx-auto w-fit md:mx-0">
            <a :href="item.link">{{ item.name }}</a>
            <div class="h-[2px] w-full origin-center scale-x-0 bg-white transition-transform duration-200 group-hover:scale-x-100"></div>
          </div>
        </div>
      </div>

      
      <div class="flex flex-col items-center space-y-8 md:space-y-6 md:items-end">
        <div class="flex flex-row space-x-6 items-center">
          <div class="group relative">
            <img src="../assets/icon-facebook.svg" alt="Facebook" class="w-6 cursor-pointer" />
            <div class="hidden md:block absolute -bottom-2 w-full h-[2px] bg-white scale-x-0 transition-transform duration-200 group-hover:scale-x-100"></div>
          </div>
          <div class="group relative">
            <img src="../assets/icon-twitter.svg" alt="Twitter" class="w-6 cursor-pointer" />
            <div class="hidden md:block absolute -bottom-2 w-full h-[2px] bg-white scale-x-0 transition-transform duration-200 group-hover:scale-x-100"></div>
          </div>
          <div class="group relative">
            <img src="../assets/icon-pinterest.svg" alt="Pinterest" class="w-6 cursor-pointer" />
            <div class="hidden md:block absolute -bottom-2 w-full h-[2px] bg-white scale-x-0 transition-transform duration-200 group-hover:scale-x-100"></div>
          </div>
          <div class="group relative">
            <img src="../assets/icon-instagram.svg" alt="Instagram" class="w-6 cursor-pointer" />
            <div class="hidden md:block absolute -bottom-2 w-full h-[2px] bg-white scale-x-0 transition-transform duration-200 group-hover:scale-x-100"></div>
          </div>
        </div>
        <div class="text-gray-500 font-sans">
          © 2021 Loopstudios. All rights reserved.
        </div>
      </div>
      
    </div>
  </footer>
</template>

<style scoped></style>