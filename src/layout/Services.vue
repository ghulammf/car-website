<script setup>
import Title from "../components/Title.vue";

import audi from "../assets/audi-logo.png";
import mercedes from "../assets/mercedes-logo.png";
import vw from "../assets/vw-logo.png";
import bmw from "../assets/bmw-logo.png";
import mercedes_s from "../assets/mercedes-services.png";
import royce from "../assets/royce-services.png";
import bentley from "../assets/bentley-services.png";
import lamborghini from "../assets/lamborghini-services.png";
import maserati from "../assets/maserati-services.png";
import ferrari from "../assets/ferrari-services.png";
import rover from "../assets/rover-services.png";
import Paragraph from "../components/Paragraph.vue";
import { ref } from "vue";

const logo = [audi, mercedes, vw, bmw];
const car = [
  { brand: "Mercedes-Benz", img: mercedes_s },
  { brand: "Rolls-Royce", img: royce },
  { brand: "Bentley", img: bentley },
  { brand: "Lamborghini", img: lamborghini },
  { brand: "Maseerati", img: maserati },
  { brand: "Ferrari", img: ferrari },
  { brand: "Range Rover", img: rover },
];

const count = ref(0);
</script>

<template>
  <div
    id="services"
    class="max-w-[90%] m-auto my-20 grid gap-6 sm:gap-10 md:gap-16"
  >
    <div class="grid grid-cols-2 gap-4 sm:grid-cols-4 md:gap-8">
      <div
        v-for="item in logo"
        class="border-2 border-dashed border-red-800 rounded-lg content-center p-3"
      >
        <img :src="item" alt="" />
      </div>
    </div>
    <div>
      <Title text="Get All Luxurius Brands Cars" />
    </div>
    <div
      class="bg-slate-950 md:flex md:h-[500px] rounded-xl overflow-hidden p-5 md:p-8"
    >
      <div
        class="flex items-center md:grid overflow-x-auto gap-3 p-5 md:w-[30%] md:overflow-auto"
      >
        <button
          v-for="(item, index) in car"
          @click="count = index"
          :style="count == index ? 'color: red; box-shadow: 0 0 5px red' : ''"
          class="text-white px-5 py-3 h-fit min-w-fit rounded-lg"
        >
          {{ item.brand }}
        </button>
      </div>
      <div class="p-5 grid gap-5 md:w-[70%] md:overflow-auto">
        <div class="bg-car rounded-lg p-3">
          <img :src="car[count].img" alt="" />
        </div>
        <h1 class="text-white text-xl font-medium">{{ car[count].brand }}</h1>
        <p class="text-white">
          {{ car[count].brand }} has been producing vehicles that combine sporty
          performance with luxuriouscomfort since the end of World War II,
          making them the obvious coice.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bg-car {
  background-color: hsla(0, 0%, 100%, 0.04);
  backdrop-filter: blur(10px);
}

::-webkit-scrollbar {
  width: 5px;
  height: 5px;
}

::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(102, 0, 0, 0.3);
}

::-webkit-scrollbar-thumb {
  background-color: rgb(127, 29, 29);
  border-radius: 5px;
  -webkit-box-shadow: inset 0 0 6px rgba(106, 0, 0, 0.5);
}
</style>
