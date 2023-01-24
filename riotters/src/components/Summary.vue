<script setup>
import Chart from "chart.js/auto"
import { getRelativePosition } from "chart.js/helpers"
import { onMounted } from "vue"

onMounted(() => {
  const ctx = document.getElementById("myChart")

  new Chart(ctx, {
    type: "line",
    data: {
      labels: ["09:00", "11:00", "13:00", "15:00", "17:00", "Orange"],
      datasets: [
        {
          label: "# of Votes",
          data: [12, 19, 3, 5, 2, 3],
          borderWidth: 1,
        },
      ],
    },
    options: {
      scales: {
        y: {
          beginAtZero: true,
        },
      },
    },
  })
})
</script>

<template>
  <div class="bg-[#F7F7F9] w-full h-full md:h-5/6 md:basis-1/2 px-4">
    <canvas id="myChart"></canvas>
  </div>
</template>

<style></style>
