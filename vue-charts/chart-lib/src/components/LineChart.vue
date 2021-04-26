<template>
  <canvas ref="lineChart" id="lineChart"></canvas>
</template>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
const labels = [
  'January',
  'February',
  'March',
  'April',
  'May',
  'June',
];
const data = {
  labels: labels,
  datasets: [{
    label: 'My First dataset',
    backgroundColor: 'rgb(255, 99, 132)',
    borderColor: 'rgb(255, 99, 132)',
    data: [0, 10, 5, 2, 20, 30, 45],
  }]
};
const config = {
  type: 'line',
  data,
  options: {}
};

export default {
    mounted() {
        var myChart = new Chart(
            this.$refs.lineChart,
            config
        );
    }
}
</script>
<style>

</style>