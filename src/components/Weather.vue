<template>
    <div class="weather-container">
        <div class="search-bar">
            <input v-model="city" @keyup.enter="getWeather" placeholder="Enter city name..." />
            <button @click="getWeather">Search</button>
        </div>

        <div v-if="weatherData" class="results">
            <h2>{{ weatherData.name }}, {{ weatherData.sys.country }}</h2>
            <p class="temp">{{ Math.round(weatherData.main.temp) }}°C</p>
            <p>{{ weatherData.weather[0].description }}</p>
        </div>

        <p v-if="error" class="error">{{ error }}</p>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import axios from 'axios';

const city = ref('');
const weatherData = ref(null);
const error = ref(null);

const apiKey = 'dbf73562aae009e20951f50b4fbefd2e'; // Replace with your real key

const getWeather = async () => {
    if (!city.value) return;

    try {
        error.value = null;
        const url = `https://api.openweathermap.org/data/2.5/weather?q=${city.value}&units=metric&appid=${apiKey}`;
        const response = await axios.get(url);
        weatherData.value = response.data;
    } catch (err) {
        error.value = "City not found. Please try again.";
        weatherData.value = null;
    }
};
</script>

<style scoped>
*{
    font-family: 'Poppins', sans-serif;
}
.weather-container {
    text-align: center;
    font-family: 'Poppins', sans-serif;
    color: rgb(33, 68, 68);
}

input {
    padding: 10px;
    border-radius: 4px;
    border: none;
    outline: none;
}
input:focus {
    box-shadow: 0 0 20px rgba(33, 68, 68, 0.8); 
}

.temp {
    font-size: 2rem;
    font-weight: bold;
}

.error {
    color: #f54a45;
}


button {
    background-color: transparent;
    border: none;
    color: #214444;
    cursor: pointer;
    font-size: 13px;
    font-weight: 600;
}
button:hover {
    text-decoration: underline;
}
</style>