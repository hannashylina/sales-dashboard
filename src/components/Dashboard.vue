<script setup>
import Card from './Card.vue'
import SalesChart from './SalesChart.vue'

const data = [
    {
        name: "Total sales",
        value: 100
    },
    {
        name: "Number of orders",
        value: 113
    },
    {
        name: "Top-performing product",
        value: 'Product 1'
    },
    {
        name: "Sales growth percentage",
        value: 1.5
    }
]
</script>

<template>
    <section>
        <h1 class="text-3xl font-bold">
            Sales Dashboard
        </h1>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 py-6 sm:py-8 grid gap-4">
            <Card v-for="(item, index) in data"
                  :data="item"
                  :key="index"></Card>
        </div>
    </section>
    <section class="flex flex-row">
        <div class="w-100 md:w-1/2 lg:w-1/3">
            <SalesChart></SalesChart>
        </div>
        <div class="w-1/2">

        </div>
    </section>
</template>

<style scoped>

</style>