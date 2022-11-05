<script setup>
</script>

<template>
  <div class="flex justify-around items-center">
    <div class="card w-96 bg-base-100 shadow-xl m-4">
      <div class="card-body">
        <div class="card-actions justify-end">
          <button class="btn btn-square btn-sm">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
        <div data-theme="light" class="m-4 p-4">
          This div will always use light theme
          <span data-theme="dark">This span will always use dark theme!</span>
        </div>
      </div>
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
</template>

<style scoped>
</style>