<script setup>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <Header msg="This is my daisyUI playground :-)" />
  <div data-theme="light">
    This div will always use light theme
    <span data-theme="dark">This span will always use dark theme!</span>
  </div>
  <Footer msg="I´m the Footer" />
</template>

<style scoped>
</style>
