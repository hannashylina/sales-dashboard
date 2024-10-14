<script setup>
import Chart from 'chart.js/auto'
import { onMounted } from "vue";

const productsData = [
    {
        name: 'Product 1',
        sales: 120
    },
    {
        name: 'Product 2',
        sales: 132
    },
    {
        name: 'Product 3',
        sales: 105
    },
    {
        name: 'Product 4',
        sales: 167
    }
]

let labels = productsData.map(item => item.name)
let sales = productsData.map(item => item.sales)

const data = {
    labels: labels,
    datasets: [{
        label: 'Top products by sales',
        data: sales,
        backgroundColor: [
            'rgb(209 250 229)',
            'rgb(167 243 208)',
            'rgb(236 253 245)',
            'rgb(110 231 183)'
        ],
        borderWidth: 0
    }]
};

const config = {
    type: 'bar',
    data: data,
    options: {
        scales: {
            y: {
                beginAtZero: true
            }
        }
    },
};

onMounted(() => {
    const ctx = document.getElementById('performance-chart')
    new Chart(ctx, config)
})

</script>

<template>
    <canvas id="performance-chart"
            width="400"
            height="400"></canvas>
</template>

<style scoped>

</style>