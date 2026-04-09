<script setup>
import Navbar from "./components/Navbar.vue";
import Feature from "./components/Feature.vue";
import Creation from "./components/Creation.vue";
import Footer from "./components/Footer.vue";
import { ref } from "vue";


const munuItems = ref([
  { name: "About", link: "#" },
  { name: "Careers", link: "#" },
  { name: "Events", link: "#" },
  { name: "Products", link: "#" },
  { name: "Supports", link: "#" },
]);
</script>

<template>
  <div class="min-h-screen">
    <Navbar :menu-items="munuItems" />
    <Feature />
    <Creation />
    <Footer :menu-items="munuItems" />
  </div>
</template>

<style scoped></style>