<script setup>
import Chart from 'chart.js/auto'
import { onMounted } from "vue";

const salesData = [
    {
        month: 'Jan',
        sales: 120
    },
    {
        month: 'Feb',
        sales: 132
    },
    {
        month: 'Mar',
        sales: 105
    },
    {
        month: 'Apr',
        sales: 167
    },
    {
        month: 'May',
        sales: 155
    },
    {
        month: 'Jun',
        sales: 147
    },
    {
        month: 'Jul',
        sales: 151
    },
    {
        month: 'Aug',
        sales: 162
    },
    {
        month: 'Sep',
        sales: 155
    }
]

let sales = salesData.map(item => item.sales)
let labels = salesData.map(item => item.month)

const config = {
    type: 'line',
    data: {
        labels: labels,
        datasets: [{
            label: 'Total sales by month',
            data: sales,
            borderWidth: 1,
            pointStyle: false,
            lineTension: 0.1,
            fill: true,
            backgroundColor: 'rgb(209 250 229)',
            borderColor: 'rgb(16 185 129)'
        }]
    },
    options: {
        scales: {
            x: {
                grid: {
                    display: false
                }
            },
            y: {
                grid: {
                    display: false
                }
            }
        },
        plugins: {
            legend: {
                font: {
                    size: 18,
                    family: ''
                }
            }
        }
    }
}

onMounted(() => {
    const ctx = document.getElementById('sales-chart')
    new Chart(ctx, config)
})

</script>

<template>
    <canvas id="sales-chart"
            width="400"
            height="400"></canvas>
</template>

<style scoped>

</style>