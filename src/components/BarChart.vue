<template>
    <div>
        <canvas ref="barChart" id="barChart" width="350" height="200"></canvas>
    </div>
</template>
<script>

export default {
    props: ['propsdata'],
    mounted() {
    // eslint-disable-next-line no-unused-vars
    const barChart = new this.$_Chart(this.$refs.barChart, {
        type: 'bar',
        data: {
            labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
            datasets: this.propsdata
        },
        options: {
            scales: {
                y: {
                    beginAtZero: true
                }
            }
        },
        onClick: function() {
            this.$emit('refresh:chart');
        }
    });
  },
}
</script>
<style>
    
</style>