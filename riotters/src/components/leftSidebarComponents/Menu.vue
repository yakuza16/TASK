<script setup>
import { ref } from "vue";

// another way is to add vue router, but in this case i choose this to show v-for loop
const links = ref([
  {
    name: "Overview",
    iconName: "home",
    isActive: true,
  },
  {
    name: "Buy/Sell",
    iconName: "bank",
    isActive: false,
  },
  {
    name: "Wallets",
    iconName: "wallet",
    isActive: false,
  },
  {
    name: "Bundles",
    iconName: "bundles",
    isActive: false,
  },
  {
    name: "Reporting",
    iconName: "flag",
    isActive: false,
  },
  {
    name: "Community",
    iconName: "community",
    isActive: false,
  },
]);

function setActive(links, id) {
  if (links[id].isActive) {
    links[id].isActive = !links[id].isActive;
  } else {
    links[id].isActive = !links[id].isActive;
  }
}
</script>

<template>
  <nav class="w-full mt-6 lg:mt-4 xl:mt-2 border-b-2 border-[#9896A1] pb-6">
    <ul class="flex flex-col space-y-4">
      <li class="w-full" v-for="(link, index) in links" :key="index">
        <button
          @click="setActive(links, index)"
          class="w-full mx-auto flex items-center space-x-7 transition-shadow ease-in delay-75 hover:shadow-md p-1"
          :class="[
            link.isActive === false
              ? 'bg-none'
              : 'bg-white relative text-black',
          ]"
        >
          <img
            class="w-4 h-6 lg:w-6 lg:h-8 ml-10"
            :src="`/${link.iconName}.svg`"
            :alt="link.iconName"
          />
          <span
            v-if="link.isActive"
            class="text-base lg:text-lg xl:text-2xl font-bold"
            >{{ link.name }}</span
          >
          <span v-else class="text-base lg:text-lg xl:text-2xl">{{
            link.name
          }}</span>
          <span
            v-show="link.isActive"
            class="bg-[#EA4D4D] text-white rounded-lg w-3 h-4 md:w-4 text-xs absolute right-1 top-1"
            >9+</span
          >
        </button>
      </li>
    </ul>
  </nav>
</template>
