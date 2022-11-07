<script setup>
  import { useToast } from "vue-toastification";
  import SkeletonPicture from "./SkeletonPicture.vue";

  const toast = useToast();
  const success = () => toast.success("You did it! 🎉");
</script>

<template>
  <div class="card">
    <div class="card w-96 rounded-2xl">
      <SkeletonPicture height="h-[216px]" />
      <div class="card-body glass rounded-b-2xl">
        <h2 class="card-title">Transparent</h2>
        <p>Lorem ipsum and more example text</p>
        <div class="card-actions justify-end">
          <button @click="success" class="btn btn-primary">Push me!</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
