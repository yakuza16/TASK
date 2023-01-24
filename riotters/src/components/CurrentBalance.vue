<script setup>
import { computed } from "vue"

const props = defineProps(["coinValue"])

const myQuantityOfCoins = 3

const myQuantityAfterConversion = computed(() => {
  return String(props.coinValue) * myQuantityOfCoins
})
</script>

<template>
  <div class="bg-[#F7F7F9]">
    <div class="flex justify-between items-baseline">
      <p class="ml-2 lg:ml-1 font-bold">Current Balance</p>
      <span class="text-base font-bold md:text-3xl">...</span>
    </div>
    <p class="text-3xl">
      <span class="text-[#9896A1]">$</span>
      <span class="font-bold" v-if="myQuantityAfterConversion">{{
        myQuantityAfterConversion
      }}</span>
      <span v-else>Pobiera dane...</span>
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
