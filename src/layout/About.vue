<script setup>
import audi from "../assets/audi-about.png";
import Paragraph from "../components/Paragraph.vue";
import Title from "../components/Title.vue";

const card = [
  {
    title: "Certified Mechanics",
    description:
      "Browse a wide selection of new and used cars from trusted dealers and selters.",
  },
  {
    title: "Popular Brands",
    description:
      "Browse a wide selection of new and used cars from trusted dealers and sellers.",
  },
  {
    title: "Reasonable Price",
    description:
      "Browse a wide selection of new and used cars from trusted dealers and sellers.",
  },
  {
    title: "Best Quality Cars",
    description:
      "Browse a wide selection of new and used cars from trusted dealers and sellers.",
  },
];
</script>

<template>
  <div
    id="about"
    class="max-w-[90%] m-auto md:flex gap-3 sm:gap-10 md:gap-16 my-10 sm:my-7 md:my-16"
  >
    <div class="flex flex-col gap-4 sm:gap-5 md:gap-6">
      <Title text="We Are Dedicated to Provide Quality Service" />
      <Paragraph
        text="At our marketplace, we bring you the best vehicles from top brands. Find
        the car that suits your style and budget"
      />
      <img :src="audi" alt="" />
    </div>
    <div class="grid grid-cols-2 gap-3">
      <div
        v-for="item in card"
        class="p-5 rounded-lg shadow-xl grid content-around gap-4 hover:bg-slate-950 hover:text-white card"
      >
        <h1 class="text-2xl font-medium">{{ item.title }}</h1>
        <p>{{ item.description }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
  transition: all;
  transition-duration: 500ms;
}
</style>
