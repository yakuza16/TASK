<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);
</script>

<template>
  <div class="bg-red-200 w-full p-1 md:flex md:items-center md:max-h-fit">
    <div class="w-full h-full py-2 flex justify-center md:justify-start">
      <input
        type="text"
        placeholder="&#xF002;    Search"
        class="p-3 w-5/6 h-full md:w-1/3 lg:w-1/6 md:ml-10 bg-[#F7F7F9] transition-colors duration-300 ease-linear rounded-lg hover:bg-gray-200"
        style="font-family: Arial, 'Font Awesome 5 Free'"
      />
    </div>
    <div class="py-2 flex justify-evenly md:justify-end md:space-x-6 md:px-6">
      <button
        class="alert w-1/3 md:h-12 md:w-max xl:w-16 bg-[#F7F7F9] p-4 rounded-lg transition-colors duration-300 ease-linear hover:bg-gray-200"
      >
        <img
          class="w-1/3 h-auto md:w-3/4 lg:w-2/3 mx-auto"
          src="/alert.svg"
          alt=""
        />
      </button>
      <button
        @click="isMenuOpen = !isMenuOpen"
        class="w-1/3 md:h-12 md:w-max xl:w-16 bg-[#F7F7F9] p-4 rounded-lg transition-colors duration-300 ease-linear hover:bg-gray-200"
      >
        <img
          class="w-1/3 h-auto md:w-3/4 lg:w-2/3 mx-auto"
          src="/ham_bar.svg"
          alt=""
        />
      </button>
    </div>
  </div>
  <div
    class="fixed w-1/2 md:w-1/3 h-screen bg-gray-200/90"
    :class="!isMenuOpen ? 'hidden' : 'show top-0 left-0 z-2'"
  >
    <nav>
      <ul>
        <li><a href="#">Link 1</a></li>
        <li><a href="#">Link 2</a></li>
        <li><a href="#">Link 3</a></li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
.alert {
  position: relative;
}
.alert::after {
  content: "";
  width: 12px;
  height: 12px;
  border-radius: 100%;
  background-color: #ea4d4d;
  position: absolute;
  top: 0;
  right: 0;
}
</style>
