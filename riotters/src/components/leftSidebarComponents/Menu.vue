<script setup>
import { ref } from "vue"

// another way is to add vue router, but in this case i choose this
const links = ref([
  {
    name: "Overview",
    iconPath: "../../assets/home.svg",
  },
  {
    name: "Buy/Sell",
    iconPath: "../../assets/bank.svg",
  },
  {
    name: "Wallets",
    iconPath: "../../assets/wallet.svg",
  },
  {
    name: "Bundles",
    iconPath: "../../assets/bundles.svg",
  },
  {
    name: "Reporting",
    iconPath: "../../assets/flag.svg",
  },
  {
    name: "Community",
    iconPath: "../../assets/community.svg",
  },
])
</script>

<template>
  <nav>
    <ul>
      <li class="w-24" v-for="(link, index) in links" :key="index">
        <div class="w-24">
          <div class="w-12">
            <img class="w-36 h-full" :src="link.iconPath" alt="" />
          </div>
          <span>{{ link.name }}</span>
        </div>
      </li>
    </ul>
  </nav>
</template>
