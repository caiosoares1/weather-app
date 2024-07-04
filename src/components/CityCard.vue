<template>
    <div class="city-card">
        <h2>{{ cityName }}</h2>
        <p>Temperature: {{ temperature }}°C</p>
        <!-- outras informações sobre a cidade aqui -->
    </div>
</template>

<script>
export default {
    props: {
        cityName: {
            type: String,
            required: true
        },
        temperature: {
            type: Number,
            required: true
        }
        // outras propriedades da cidade aqui
    }
}
</script>

<style scoped>
.city-card {
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 16px;
    margin-bottom: 16px;
}
</style>