<script setup>
import MainMenu from "./MainMenu.vue"
import CurrentBalance from "./CurrentBalance.vue"
import Summary from "./Summary.vue"

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
      class="flex flex-col p-2 space-y-3 md:p-11 md:flex-row h-1/3 md:h-3/6 md:items-baseline bg-red-100 md:space-x-8"
    >
      <CurrentBalance :coinValue="cryptoData" />
      <Summary />
    </div>
  </div>
</template>
