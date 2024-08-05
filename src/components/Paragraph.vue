<script setup>
const props = defineProps(["text"]);
</script>

<template>
  <div>
    <p class="text-lg sm:text-1xl md:text-2xl">{{ props.text }}</p>
  </div>
</template>
