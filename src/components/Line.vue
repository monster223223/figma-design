<template>
    <Line :data="data" :options="options" />
  </template>
  
  <script lang="ts">
  import {
    Chart as ChartJS,
    CategoryScale,
    LinearScale,
    PointElement,
    LineElement,
    Title,
    Tooltip,
    Legend,
    Filler
  } from 'chart.js'
  import { Line } from 'vue-chartjs'
  import * as lineChartConfig from './lineChartConfig.js'
  
  ChartJS.register(
    CategoryScale,
    LinearScale,
    PointElement,
    LineElement,
    Title,
    Tooltip,
    Legend,
    Filler
  )
  
  export default {
    name: 'App',
    components: {
      Line
    },
    data() {
      return lineChartConfig
    }
  }
  </script>
  