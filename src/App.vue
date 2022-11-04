<script setup>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <Header msg="This is my daisyUI playground :-)" />
  <div class="flex justify-around">
    <div data-theme="light" class="m-4 p-4">
      This div will always use light theme
      <span data-theme="dark">This span will always use dark theme!</span>
    </div>
    <div>
      <p class="text-center text-lg">Good or Bad?</p>
      <label class="swap swap-flip text-9xl">
        <input type="checkbox" />
        <div class="swap-on">😈</div>
        <div class="swap-off">😇</div>
      </label>
    </div>
  </div>
  <Footer msg="I´m the Footer" />
</template>

<style scoped>
</style>
