<script setup>
import LeftSidebar from "./LeftSidebar.vue"
import MainContent from "./MainContent.vue"
</script>

<template>
  <div class="w-full h-screen bg-white rounded-3xl flex">
    <LeftSidebar class="w-1/2 md:w-2/3 lg:w-1/5" />
    <MainContent class="w-full p-12" />
  </div>
</template>

<style scoped></style>
