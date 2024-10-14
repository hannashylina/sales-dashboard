<script setup>
const props = defineProps({
    data: Object
})
</script>

<template>
    <div class="">
        <div class="">
            <p>{{data.name}}</p>
            <p>{{data.value}}</p>
        </div>
    </div>
</template>

<style scoped>

</style>