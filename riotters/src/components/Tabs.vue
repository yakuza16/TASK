<script setup>
import CoinInfo from "./CoinInfo.vue"
import { ref } from "vue"
const props = defineProps(["isActive"])
const tabs = ref(["Summary", "Table", "Charts", "Reporting", "Analysis"])
</script>

<template>
  <div class="w-full bg-[#F7F7F9] h-full rounded-lg">
    <ul
      class="flex flex-col md:flex-row w-full border-b-2 space-x-3 h-4 md:h-12 text-[#9896A1]"
    >
      <li
        class="first:font-bold first:border-b-2 md:px-6 md: md:pt-3 first:border-[#7445FB] first:text-black"
        v-for="(tab, id) in tabs"
        :key="id"
      >
        <a class="p-2" href="#">{{ tab }}</a>
      </li>
    </ul>
    <div>
      <CoinInfo />
    </div>
  </div>
</template>
