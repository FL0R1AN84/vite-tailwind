<script setup>
  import { ref } from "vue";
  import CarouselVue from "./Carousel.vue";
  import CarouselVerticalVue from "./CarouselVertical.vue";

  const vertical = ref(true);
</script>

<template>
  <div class="mockup-phone">
    <div class="camera"></div>
    <div class="display">
      <div v-if="!vertical" class="artboard artboard-demo phone-1">
        <CarouselVue />
      </div>
      <div v-if="vertical" class="artboard artboard-demo phone-1">
        <CarouselVerticalVue />
      </div>
    </div>
    <div class="flex justify-center relative bottom-32 opacity-90">
      <button @click="vertical = !vertical" class="btn">
        {{ vertical }}
      </button>
    </div>
  </div>
</template>

<style scoped></style>
