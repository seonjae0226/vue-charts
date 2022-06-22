<template>
    <div>
        <canvas ref="lineChart" id="lineChart"></canvas>
    </div>
</template>
<script>

export default {
    mounted() {
        // eslint-disable-next-line no-unused-vars
        const lineChart = new this.$_Chart(this.$refs.lineChart.getContext('2d'),{
            type: 'line',
            data: {
                labels: ['January','February','March','April','May','June'],
                datasets: [{
                    label: 'My First dataset',
                    data: [0, 10, 5, 2, 20, 30, 45],
                    backgroundColor: 'rgb(255, 99, 132)',
                    borderColor: 'rgb(255, 99, 132)',
                }]
            },
            options: {}

        });
    },
}
</script>
<style>
    
</style>