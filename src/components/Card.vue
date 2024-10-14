<script setup>
const props = defineProps({
    data: Object
})
</script>

<template>
    <div class="flex items-stretch flex-row-reverse justify-end">
        <p class="p-4 grow">{{data.name}}</p>
        <p class="p-4 flex-none">{{data.value}}</p>
    </div>
</template>

<style scoped>

</style>