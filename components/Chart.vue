<script setup lang="ts">
import Chart from "chart.js/auto";

const labels = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
const data = {
  labels: labels,
  datasets: [
    {
      label: "Pengunjung",
      data: [80, 20, 60, 25, 45, 17, 55, 100, 59, 35, 25, 79],
      backgroundColor: ["#1876cd"],
    },
  ],
};
const config = {
  type: "bar",
  data: data,
  options: { responsive: true, maintainAspectRatio: false, aspectRatio: 0.7 },
};

onMounted(() => {
  const myChart = new Chart(document.getElementById("myChart"), config);
});
</script>

<template>
  <div>
    <canvas id="myChart"></canvas>
  </div>
</template>
