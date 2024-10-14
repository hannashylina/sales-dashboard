<script setup>
import Card from './Card.vue'

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
        <div class="grid grid-cols-1 sm:grid-cols-4 py-6 sm:py-8 grid gap-4">
            <Card v-for="(item, index) in data"
                  :data="item"
                  :key="index"></Card>
        </div>
    </section>
</template>

<style scoped>

</style>