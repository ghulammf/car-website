<script setup>
const fieldCategory = [
  {
    placeholder: "Search by Keywords",
  },
  {
    placeholder: "All Brands",
  },
  {
    placeholder: "All Models",
  },
  {
    placeholder: "Budgets",
  },
];
</script>

<template>
  <div
    class="grid gap-4 md:gap-6 lg:gap-8 max-w-[80%] m-auto bg-white rounded-xl shadow-lg -translate-y-1/4 sm:-translate-y-1/3 md:-translate-y-1/2 p-5"
  >
    <div>
      <h1 class="text-center font-bold text-2xl md:text-3xl">
        Search our 30000 vehicles
      </h1>
    </div>
    <div class="flex gap-2 justify-around flex-wrap">
      <input
        class="basis-1 h-9 ps-3 flex-1 rounded-lg border-2"
        v-for="item in fieldCategory"
        type="text"
        :placeholder="item.placeholder"
      />
      <button class="bg-red-800 px-6 h-9 rounded-md text-white font-medium">
        Search
      </button>
    </div>
  </div>
</template>
