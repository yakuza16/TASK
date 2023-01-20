<script setup></script>

<template>
  <div class="w-full mt-6 lg:mt-4 xl:mt-2 flex flex-col text-lg">
    <div class="flex justify-evenly items-end md:space-x-20 lg:space-x-32">
      <p class="ml-2 lg:ml-1">Favorites</p>
      <span class="text-base font-bold md:text-3xl">...</span>
    </div>
  </div>
  <div>
    <ul class="flex flex-col justify-center">
      <li class="flex items-center justify-evenly space-y-4">
        <div><img src="../../../public/bitcoin.png" alt="ikona BTC" /></div>
        <div class="flex flex-col items-left pr-10">
          <p>BCT</p>
          <p class="font-bold text-black">Bitcoin</p>
        </div>
        <div><img src="" alt="wykres" /></div>
      </li>
      <li class="flex items-center justify-evenly space-y-6">
        <div><img src="../../../public/ripple.png" alt="ikona BTC" /></div>
        <div class="flex flex-col items-left pr-10">
          <p>XRP</p>
          <p class="font-bold text-black">Ripple</p>
        </div>
        <div><img src="" alt="wykres" /></div>
      </li>
    </ul>
  </div>
</template>

<style scoped></style>
