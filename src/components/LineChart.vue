<template>
  <canvas ref="lineChart" id="lineChart"></canvas>
</template>

<script>

export default {
  mounted() {
    //ref 적용 
      // var ctx = this.$refs.lineChart.getContext('2d');
      var ctx = this.$refs.lineChart.getContext('2d');
      // eslint-disable-next-line no-unused-vars
      var chart = new this.$_Chart(ctx, {
          // The type of chart we want to create
          type: 'line',

          // The data for our dataset
          data: {
              labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
              datasets: [{
                  label: 'My First dataset',
                  backgroundColor: 'rgb(255, 99, 132)',
                  borderColor: 'rgb(255, 99, 132)',
                  data: [0, 10, 5, 2, 20, 30, 45]
              }]
          },

          // Configuration options go here
          options: {}
      });
      // eslint-disable-next-line no-console
      console.log(this.$_Chart);
    },
  }

</script>

<style>

</style>