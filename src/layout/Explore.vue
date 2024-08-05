<script setup>
import Title from "../components/Title.vue";
// brand logo
import audi from "../assets/audi-logo.png";
import bmw from "../assets/bmw-logo.png";
import mercedes from "../assets/mercedes-logo.png";
import vw from "../assets/vw-logo.png";
// car
import audix from "../assets/audi-explore.png";
import bmwx from "../assets/bmw-explore.png";
import mercedesx from "../assets/mercedes-explore.png";

const brandLogo = [
  { img: audi, brand: "Audi" },
  { img: bmw, brand: "BMW" },
  { img: mercedes, brand: "Mercedes" },
  { img: vw, brand: "Volkswegen" },
  { img: "", brand: "Explore 10+" },
];

const card = [
  {
    img: audix,
    title: "Audi Q4 Sportback e-tron",
    release: "Release 21 Feb 2022",
    price: "$52,000",
  },
  {
    img: bmwx,
    title: "BMW 2 Series Gran Coupe",
    release: "Release 15 Jun 2021",
    price: "$45,000",
  },
  {
    img: mercedesx,
    title: "Mercedes-Benz Spinter",
    release: "Release 28 May 2023",
    price: "$48,000",
  },
];
</script>

<template>
  <div
    id="stock"
    class="max-w-[90%] m-auto py-20 grid gap-4 sm:gap-8 md:gap-12"
  >
    <div>
      <Title text="Explore Our Vehicle" style="text-align: center" />
    </div>
    <div class="m-auto flex w-[90%] justify-center gap-5 overflow-auto py-4">
      <div
        v-for="item in brandLogo"
        class="flex border-2 min-w-fit py-2 px-3 gap-3 rounded-lg cursor-pointer hover:bg-slate-950 hover:text-white"
      >
        <img :src="item.img" alt="" class="h-7" />
        <p class="content-center">{{ item.brand }}</p>
      </div>
    </div>
    <div class="grid gap-5 min-[550px]:grid-cols-2 md:grid-cols-3">
      <div
        class="shadow-lg px-4 py-5 grid gap-4 rounded-lg"
        v-for="item in card"
      >
        <div>
          <img :src="item.img" alt="" />
        </div>
        <h1 class="font-bold text-lg">{{ item.title }}</h1>
        <p class="text-slate-400">{{ item.release }}</p>
        <div class="flex justify-between items-center">
          <p class="font-semibold">{{ item.price }}</p>
          <button class="py-2 px-3 bg-red-800 text-white rounded-md">
            Discover
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
::-webkit-scrollbar {
  width: 5px;
  height: 5px;
}

::-webkit-scrollbar-thumb {
  background-color: rgb(17, 24, 39);
  border-radius: 5px;
  -webkit-box-shadow: inset 0 0 6px rgba(106, 0, 0, 0.5);
}
</style>
