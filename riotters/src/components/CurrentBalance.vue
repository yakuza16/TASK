<script setup>
import { ref, onMounted } from "vue"

const cryptoData = ref(null)

onMounted(() => {
  fetch(`https://api.coinpaprika.com/v1/tickers/btc-bitcoin`)
    .then((response) => response.json())
    .then((data) => (cryptoData.value = data.quotes.USD.price))
})
</script>

<template>
  <div
    class="bg-[#F7F7F9] w-full h-full md:h-5/6 md:basis-1/2 px-4 flex flex-col justify-around"
  >
    <div class="flex justify-between items-center">
      <p class="ml-2 lg:ml-1">Current Balance</p>
      <span class="text-base font-bold md:text-3xl">...</span>
    </div>
    <p class="text-3xl">
      <span class="text-[#9896A1]">$</span
      ><span class="font-bold">21 432.23 </span
      ><span v-if="cryptoData">{{ cryptoData }}</span>
      <span v-else>Ładuje się</span>
    </p>
    <p class="flex">
      <span><img src="/arrow_up.svg" alt="arrow up" /></span
      ><span class="text-[#2DC78F]">12% vs last month</span>
    </p>
    <div class="flex md:space-x-5 text-xs md:text-lg md:font-bold">
      <button class="text-white bg-[#7445FB] rounded p-1 md:p-4 border">
        Quick Invest
      </button>
      <button class="bg-white text-[#7445FB] rounded p-1 md:p-4 border">
        Show Report
      </button>
    </div>
  </div>
</template>

<style></style>
