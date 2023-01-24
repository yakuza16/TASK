<script setup>
import MainMenu from "./MainMenu.vue"
import CurrentBalance from "./CurrentBalance.vue"
import Summary from "./Summary.vue"
import Tabs from "./Tabs.vue"

import { ref, onMounted } from "vue"

const cryptoData = ref(null)

function fetchCryptoData() {
  fetch(`https://api.coinpaprika.com/v1/tickers/btc-bitcoin`)
    .then((response) => response.json())
    .then((data) => (cryptoData.value = data.quotes.USD.price))
}

onMounted(() => {
  fetchCryptoData()
})
</script>

<template>
  <div>
    <MainMenu />
    <div
      class="flex flex-col p-2 space-y-3 md:p-11 md:flex-row h-1/3 md:h-3/6 md:items-baseline md:flex-wrap bg-red-100 md:baseline"
    >
      <CurrentBalance
        :coinValue="cryptoData"
        class="order-1 w-full h-full md:h-5/6 md:basis-1/2 px-4 flex flex-col justify-around"
      />
      <Summary
        class="order-3 md:order-2 w-full h-full md:h-5/6 md:basis-1/2 px-4"
      />
      <Tabs class="order-3 md:order-3 md:basis-full" />
    </div>
  </div>
</template>
