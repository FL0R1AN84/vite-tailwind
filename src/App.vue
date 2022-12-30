<script setup>
import { ref } from "vue";
import { Modal } from "flowbite-vue";
import Header from "./components/Header.vue";
// import Footer from "./components/Footer.vue";

const count = ref(0);

const isShowModal = ref(false);
function closeModal() {
  isShowModal.value = false;
}
function showModal() {
  isShowModal.value = true;
}
</script>
<template>
  <div class="p-2">
    <button
      @click="count++"
      type="button"
      class="inline-flex relative items-center p-3 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
    >
      <svg
        class="w-6 h-6"
        fill="none"
        stroke="currentColor"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
        ></path>
      </svg>
      <span class="sr-only">Notifications</span>
      <div
        class="inline-flex absolute -top-2 -right-2 justify-center items-center w-6 h-6 text-xs font-bold text-white bg-red-500 rounded-full border-2 border-white dark:border-gray-900"
      >
        {{ count }}
      </div>
    </button>

    <Header msg="Header" />
  </div>

  <button
    @click="showModal"
    type="button"
    class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
  >
    Show modal
  </button>

  <div @click="closeModal">
    <Modal size="lg" v-if="isShowModal">
      <template #header>
        <div class="flex justify-between">
          <div class="flex items-center text-lg">Add or decrease count</div>
        </div>
      </template>
      <template #body>
        <p class="text-base leading-relaxed text-gray-500 dark:text-gray-400">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
        </p>
        <p class="text-sm leading-relaxed text-gray-400 dark:text-gray-200">
          Rerum sunt eligendi facilis dolore porro quisquam earum, tempore, fuga
          placeat quis totam autem qui doloremque corporis eaque ipsa minus.
        </p>
      </template>
      <template #footer>
        <div class="flex justify-between">
          <button
            @click="count--"
            type="button"
            class="text-gray-500 bg-white hover:bg-gray-100 focus:ring-4 focus:outline-none focus:ring-blue-300 rounded-lg border border-gray-200 text-sm font-medium px-5 py-2.5 hover:text-gray-900 focus:z-10 dark:bg-gray-700 dark:text-gray-300 dark:border-gray-500 dark:hover:text-white dark:hover:bg-gray-600 dark:focus:ring-gray-600"
          >
            Decrease count
          </button>
          <button
            @click="count++"
            type="button"
            class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
          >
            Add count
          </button>
        </div>
      </template>
    </Modal>
  </div>
</template>

<style scoped></style>
