<script>
import { Doughnut, mixins } from "vue-chartjs";

const { reactiveProp } = mixins;

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  mixins: [mixins],
  legend: {
    labels: {
      boxWidth: 10,
      fontSize: 10,
    }
  }
};

export default {
  extends: Doughnut,
  props: ["chartData", "chartOptions"],
  mixins: [reactiveProp],
  computed: {
    updateChartOptions() {
      return {
        ...chartOptions,
        ...this.chartOptions
      };
    }
  },
  mounted() {
    this.renderChart(this.chartData, this.updateChartOptions);
  }
};
</script>
