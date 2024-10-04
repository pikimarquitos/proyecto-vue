<template>
    <h3>La temperatura actual es: {{ weatherStore.temperatura }}º</h3> 
</template>
<script setup>
    import { useWeather } from '@/composables/useWeather';
    import { onMounted } from 'vue';
    import { useWeatherStore } from '@/stores/wheaterStore';

    const weatherStore = useWeatherStore();

    onMounted(() => {
        useWeather();
    })
</script>

<style scoped>

</style>