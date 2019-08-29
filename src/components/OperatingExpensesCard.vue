<template>
  <div class="operating-expenses-container tile">
    <div class="tile-header">
      <h4>Operating Expenses</h4>
    </div>
    <div class="tile-content">
      <ChartPie v-if="loaded" :height="211" :chartData="chartData" :chartOptions="chartOptions"></ChartPie>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import ChartPie from './ChartPie.vue'

@Component({
  components: {
    ChartPie
  }
})
export default class NavBar extends Vue {
  private loaded = false
  private chartData = {
    datasets: [
      {
        data: [20 , 30, 50, 10 , 60, 80],
        backgroundColor: ['#A9CCE3', '#EDBB99', '#D7BDE2', '#E6B0AA', '#E5E7E9', '#F9E79F'] }
      ],
      labels: [
        'Salaries & Personnel',
        'Repairs & Maintenance',
        'Contract Services',
        'Marketing & Advertising',
        'Administrative',
        'Utilities'
      ]
    }

  private chartOptions: object = {
    responsive: true,
    maintainAspectRatio: false,
  }

  private mounted() {
    setTimeout(() => {
      this.loaded = true
    }, 500)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>