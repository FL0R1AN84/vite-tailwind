<script setup>
  import { useToast } from "vue-toastification";

  const toast = useToast();
  const success = () => toast.success("You did it! 🎉");
</script>

<template>
  <div
    class="card"
    style="background-image: url(https://placeimg.com/400/225/arch)"
  >
    <div class="card w-96 glass">
      <figure>
        <img src="https://placeimg.com/400/225/arch" alt="random pictures" />
      </figure>
      <div class="card-body">
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
