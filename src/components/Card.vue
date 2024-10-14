<script setup>
const props = defineProps({
    data: Object
})
</script>

<template>
    <div class="flex items-stretch flex-row justify-start shadow-md rounded-md">
        <p class="p-4 flex w-1/3 items-center justify-center bg-emerald-600/75 text-white rounded-l-md">{{data.value}}</p>
        <p class="py-4 px-6 grow flex items-center">{{data.name}}</p>
    </div>
</template>

<style scoped>

</style>