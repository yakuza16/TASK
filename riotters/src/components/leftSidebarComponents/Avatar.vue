<script setup>
defineProps({
  name: String,
})
</script>

<template>
  <div
    class="mx-auto max-w-full flex place-items-end justify-evenly mb-8 space-x-4 w-full h-full"
  >
    <div class="hidden lg:block">
      <img src="/avatar.png" alt="zdjecie" />
    </div>
    <div>
      <div class="flex flex-col justify-center">
        <p>{{ name }}</p>
        <p class="font-bold text-black">marc@riot.com</p>
      </div>
    </div>
    <span class="text-base font-bold md:text-3xl">...</span>
  </div>
</template>
