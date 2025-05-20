<script setup>
import ArrowButton from '@/components/common/ArrowButton.vue';
</script>

<template>
    <div class="d-flex justify-content-center align-items-center vh-100">
        <ArrowButton direction="left" :disabled="false"/>
        <ArrowButton direction="left" :disabled="true"/>
    </div>
</template>

<style scoped>
</style>