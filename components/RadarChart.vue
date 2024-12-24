<script setup lang="ts">
import ApexCharts, { type ApexOptions } from "apexcharts";

// interface RadarChartProps {
//   id: string;
// }

// const props = defineProps<RadarChartProps>();

let Options: ApexOptions = {
  chart: {
    height: 350,
    width: "100%",
    type: "radar",
    stacked: false,
    toolbar: {
      show: false,
    },
  },
  dataLabels: {
    enabled: false,
  },
  series: [
    {
      name: "Series 1",
      data: [80, 50, 30, 40, 100, 20],
    },
  ],
  yaxis: {
    stepSize: 20,
  },
  xaxis: {
    categories: ["January", "February", "March", "April", "May", "June"],
  },
};

nextTick(() => {
    const radarChart = new ApexCharts(document.querySelector("#chart"), Options);
    radarChart.render();
});
</script>

<template>
  <div class="overflow-hidden"></div>
</template>
