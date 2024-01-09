<template>
  <div class="sales-chart">
    <line-chart :chartData="chartData" :options="chartOptions"></line-chart>
  </div>
</template>

<script>
import { Line } from 'vue-chartjs';

export default {
  components: {
    LineChart: Line
  },
  props: {
    chartData: {
      type: Object,
      required: true
    },
    chartOptions: {
      type: Object,
      default: () => ({
        responsive: true,
        maintainAspectRatio: false
      })
    }
  }
}
</script>
