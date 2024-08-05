<script setup>
import logoipsum from "../assets/logoipsum.svg";
import { ref } from "vue";

const link = [
  {
    title: "Home",
    id: "#",
  },
  {
    title: "About Us",
    id: "#about",
  },
  {
    title: "Services",
    id: "#services",
  },
  {
    title: "Stock",
    id: "#stock",
  },
  {
    title: "Contact",
    id: "#contact",
  },
];

const showNav = ref(false);
</script>

<template>
  <header
    class="h-16 md:h-20 flex justify-between px-[7%] items-center py-3 w-full fixed top-0 bg-slate-950 z-10"
  >
    <div class="">
      <img :src="logoipsum" alt="" />
    </div>
    <div class="hidden sm:flex md:text-lg gap-5 text-white">
      <a v-for="item in link" :href="item.id" class="link">{{ item.title }}</a>
    </div>
    <div class="cursor-pointer sm:hidden" @click="showNav = !showNav">
      <div class="text-4xl togle-btn" v-if="showNav">&#128938;</div>
      <div class="text-3xl togle-btn" v-else>&#9776;</div>
    </div>
    <div
      class="sm:hidden grid gap-4 absolute right-0 w-full p-5 top-16 backdrop-blur bg-slate-950 rounded-b-xl"
      v-show="showNav"
    >
      <a
        v-for="item in link"
        :href="item.id"
        class="text-red-800 font-medium text-center"
        >{{ item.title }}</a
      >
    </div>
  </header>
</template>

<style scoped>
.togle-btn,
.link {
  color: white;
  text-shadow: 0 0 2px black;
}
</style>
