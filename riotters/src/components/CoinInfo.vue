<script setup></script>

<template>
  <div class="flex justify-around items-center py-4">
    <div class="">
      <div><img src="/bitcoin.png" alt="ikona BTC" /></div>
      <div class="flex flex-col items-left pr-10">
        <p>BCT</p>
        <p class="font-bold text-black">Bitcoin</p>
      </div>
    </div>
    <div class="flex flex-col items-left pr-10">
      <p>Price</p>
      <p class="font-bold text-black">Actual Price from API</p>
    </div>
    <div class="flex flex-col items-left pr-10">
      <p>Change</p>
      <p class="font-bold text-black">Change from API</p>
    </div>
    <div><img src="" alt="wykres" /></div>
    <div class="flex space-x-3">
      <button class="bg-white text-[#7445FB] rounded p-1 md:p-4 border">
        Sell</button
      ><button class="text-white bg-[#7445FB] rounded p-1 md:p-4 border">
        Buy
      </button>
    </div>
  </div>
</template>
