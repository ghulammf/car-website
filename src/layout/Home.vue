<script setup>
import audi from "../assets/audi-home.png";
import SearchCategory from "../components/SearchCategory.vue";
</script>

<template>
  <div id="" class="bg-slate-950 pt-20 pb-10 md:py-20 w-full">
    <div class="gap-10 lg:flex max-w-[90%] m-auto">
      <div class="grid gap-5 py-7 lg:w-[40%] sm:gap-6">
        <div>
          <h1 class="text-white text-6xl font-semibold">
            Drive Home with Your <span class="text-red-700">Perfect Car</span>
          </h1>
        </div>
        <div>
          <p class="text-white text-lg sm:text-1xl md:text-2xl">
            Get behind the wheel of your dream car. Explore our extensive
            inventory and the first step towards your next adventure
          </p>
        </div>
        <div class="grid gap-4 min-[400px]:flex sm:gap-8 h-fit">
          <button class="bg-red-800 p-3 rounded-md font-semibold text-white">
            Explore More
          </button>
          <button class="bg-white p-3 rounded-md font-semibold">
            Watch Video
          </button>
        </div>
      </div>
      <div class="p-7 lg:w-[60%]">
        <img :src="audi" alt="" />
      </div>
    </div>
  </div>
  <SearchCategory />
</template>
