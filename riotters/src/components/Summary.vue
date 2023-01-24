<script setup>
import Chart from "chart.js/auto"
import { onMounted } from "vue"

onMounted(() => {
  const ctx = document.getElementById("myChart")

  new Chart(ctx, {
    type: "line",
    data: {
      labels: ["", "", "", "", "", ""],
      datasets: [
        {
          label: "This month",
          data: [12, 19, 3, 5, 2, 3],
          borderWidth: 5,
          backgroundColor: "#7445FB",
          borderColor: "#7445FB",
          showLine: true,
          pointStyle: "line",
          pointBorderWidth: 2,
          hoverBackgroundColor: "red",
        },
        {
          label: "Last month",
          data: [5, 3, 11, 0, 5, 6],
          borderWidth: 2,
          backgroundColor: "#D5D5D6",
          showLine: true,
          pointStyle: "line",
          pointBorderWidth: 2,
        },
      ],
    },

    options: {
      plugins: {
        legend: {
          display: true,
          position: "bottom",
        },
      },
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
  <div class="bg-[#F7F7F9]">
    <div class="flex justify-between items-baseline">
      <p class="ml-2 lg:ml-1 font-bold">Summary</p>
      <span class="text-base font-bold md:text-3xl">...</span>
    </div>
    <canvas id="myChart"></canvas>
  </div>
</template>

<style></style>
