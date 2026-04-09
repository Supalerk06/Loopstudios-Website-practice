<script setup>
import { ref } from 'vue';

const creationsRow1 = [
  { title: "Deep earth", mobile: "/src/assets/mobile/image-deep-earth.jpg", desktop: "/src/assets/desktop/image-deep-earth.jpg" },
  { title: "Night arcade", mobile: "/src/assets/mobile/image-night-arcade.jpg", desktop: "/src/assets/desktop/image-night-arcade.jpg" },
  { title: "Soccer team VR", mobile: "/src/assets/mobile/image-soccer-team.jpg", desktop: "/src/assets/desktop/image-soccer-team.jpg" },
  { title: "The grid", mobile: "/src/assets/mobile/image-grid.jpg", desktop: "/src/assets/desktop/image-grid.jpg" },
];

const creationsRow2 = [
  { title: "From up above VR", mobile: "/src/assets/mobile/image-from-above.jpg", desktop: "/src/assets/desktop/image-from-above.jpg" },
  { title: "Pocket borealis", mobile: "/src/assets/mobile/image-pocket-borealis.jpg", desktop: "/src/assets/desktop/image-pocket-borealis.jpg" },
  { title: "The curiosity", mobile: "/src/assets/mobile/image-curiosity.jpg", desktop: "/src/assets/desktop/image-curiosity.jpg" },
  { title: "Make it fisheye", mobile: "/src/assets/mobile/image-fisheye.jpg", desktop: "/src/assets/desktop/image-fisheye.jpg" },
];
</script>

<template>
  <section id="creations">
    <div class="container mx-auto my-32 px-6 text-gray-900 max-w-6xl md:px-0">
      
      <div class="flex flex-row justify-center mb-10 md:justify-between">
        <h2 class="text-4xl text-center uppercase md:text-left md:text-5xl">
          Our Creations
        </h2>
        
        
        <button class="hidden md:block px-10 py-2 my-0 font-bold tracking-widest uppercase border-2 border-black hover:bg-black hover:text-white">
          See All
        </button>
      </div>
      
      <div class="flex flex-col justify-between w-full space-y-6 text-2xl text-white uppercase md:flex-row md:space-y-0 md:space-x-8 mb-6 md:mb-8">
        
        <div v-for="(item, index) in creationsRow1" :key="index" class="group relative overflow-hidden md:w-1/4">

          <img class="hidden w-full duration-200 md:block group-hover:scale-110" :src="item.desktop" :alt="item.title" />

          <img class="w-full md:hidden" :src="item.mobile" :alt="item.title" />
          

          <div class="absolute top-0 bottom-0 left-0 right-0 bg-linear-to-b from-transparent to-gray-900 group-hover:from-gray-50 group-hover:to-white group-hover:opacity-70"></div>
          

          <h5 class="absolute px-6 w-52 bottom-4 md:bottom-8 md:px-10 duration-200 group-hover:scale-110 group-hover:text-black">
            {{ item.title }}
          </h5>
        </div>
      </div>

      <div class="flex flex-col justify-between w-full space-y-6 text-2xl text-white uppercase md:flex-row md:space-y-0 md:space-x-8">
        <div v-for="(item, index) in creationsRow2" :key="index" class="group relative overflow-hidden md:w-1/4">

          <img class="hidden w-full duration-200 md:block group-hover:scale-110" :src="item.desktop" :alt="item.title" />

          <img class="w-full md:hidden" :src="item.mobile" :alt="item.title" />
          

          <div class="absolute top-0 bottom-0 left-0 right-0 bg-linear-to-b from-transparent to-gray-900 group-hover:from-gray-50 group-hover:to-white group-hover:opacity-70"></div>
          

          <h5 class="absolute px-6 w-52 bottom-4 md:bottom-8 md:px-10 duration-200 group-hover:scale-110 group-hover:text-black">
            {{ item.title }}
          </h5>
        </div>
      </div>

      <div class="flex justify-center mt-10 md:hidden">
        <button class="w-full px-10 py-2 my-0 font-bold tracking-widest uppercase border-2 border-black hover:bg-black text-black hover:text-white duration-200">
          See All
        </button>
      </div>

    </div>
  </section>
</template>

<style scoped></style>