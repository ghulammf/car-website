<script setup>
const props = defineProps(["text"]);
</script>

<template>
  <div>
    <h1 class="text-4xl sm:text-5xl md:text-6xl font-semibold">
      {{ props.text }}
    </h1>
  </div>
</template>
