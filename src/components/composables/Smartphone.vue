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
        <div>
          <svg
            class="h-6 w-6 fill-current md:h-8 md:w-8"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
          >
            <path
              d="M8.59,16.58L13.17,12L8.59,7.41L10,6L16,12L10,18L8.59,16.58Z"
            ></path>
          </svg>
        </div>
      </div>
      <div v-if="vertical" class="artboard artboard-demo phone-1">
        <CarouselVerticalVue />
        <div>
          <svg
            class="h-6 w-6 fill-current md:h-8 md:w-8 rotate-90"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
          >
            <path
              d="M8.59,16.58L13.17,12L8.59,7.41L10,6L16,12L10,18L8.59,16.58Z"
            ></path>
          </svg>
        </div>
      </div>
    </div>
    <div class="flex justify-center relative bottom-24 opacity-90">
      <button @click="vertical = !vertical" class="btn">
        <span v-if="vertical">Change slide direction</span>
        <span v-if="!vertical">Change slide direction</span>
      </button>
    </div>
  </div>
</template>

<style scoped></style>
