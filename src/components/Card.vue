<script setup>
const props = defineProps({
    data: Object
})
</script>

<template>
    <div class="flex items-stretch flex-row-reverse justify-end shadow">
        <p class="p-4 grow flex items-center">{{data.name}}</p>
        <p class="p-4 flex w-1/3 items-center justify-center">{{data.value}}</p>
    </div>
</template>

<style scoped>

</style>