<script setup>
import { ref } from 'vue';

const isFlipped = ref(false);

const toggleCard = () => {
    isFlipped.value = !isFlipped.value;
};

const clubs = ref([
    { id: 1, name: 'CES' },
    { id: 2, name: 'Badminton Club' },  
    { id: 3, name: 'Tourist Club' },
    { id: 4, name: 'Art Club' },
    { id: 5, name: 'Science Club' },
]);

// This tracks which club is currently selected in the dropdown
const selectedClub = ref(clubs.value[0]);
</script>
<template>
    <div class="digital-id-container">

        <div class="selection-container">
            <div class="label-box">
                Select a club to view Digital ID:
            </div>

            <div class="dropdown-wrapper">
                <select v-model="selectedClub" class="club-dropdown">
                    <option v-for="club in clubs" :key="club.id" :value="club">
                        {{ club.name }}
                    </option>
                </select>
            </div>
        </div>

        <div class="scene">
            <div class="card" :class="{ 'is-flipped': isFlipped }">

                <div class="card__face card__face--front">
                    <img src="@/assets/front.png" alt="">
                </div>

                <div class="card__face card__face--back">
                    <img src="@/assets/back.png" alt="">

                </div>

            </div>

            <button v-if="true" @click="toggleCard" class="flip-button">
                <span>Click to flip the ID <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M4 16h13M4 16l4-4m-4 4 4 4M20 8H7m13 0-4 4m4-4-4-4" />
                    </svg>
                </span>
            </button>
        </div>

    </div>
</template>
<style scoped>
* {
    font-family: 'Poppins', sans-serif;
}

.digital-id-container {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 75.5%;
    width: 95%;
    margin-top: 40px;

}

.scene {
    position: relative;
    width: 40%;
    height: 70%;
    perspective: 800px;

}

.card {
    width: 100%;
    height: 100%;
    position: relative;
    transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
    transform-style: preserve-3d;
}

.card.is-flipped {
    transform: rotateY(180deg);
}

.card__face {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
}

.card__face--back {
    transform: rotateY(180deg);
}

.flip-button {
    margin-top: 10px;
    padding: 8px 16px;
    cursor: pointer;
    position: absolute;
    bottom: 0;
    right: 0;
    width: 200px;
    background-color: transparent;
    border: solid 1px #ffffff;
    border-radius: 10px;
}

.flip-button span {
    font-size: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 8px;
    color: #ffffff;
    font-weight: 500;
}

img {
    width: 100%;
    height: 80%;
    object-fit: cover;
    border-radius: 30px;
}

.selection-container {
    position: absolute;
    top: 0;
    left: 0;
    display: flex;
    margin-bottom: 30px;
    align-items: center;
    width: 45%;
    height: 8%;
    justify-content: space-between;
    padding-right: 20px;
}

/* The "Select a club..." white box */
.label-box {
    background: white;
    padding: 12px 25px;
    border-radius: 12px;
    font-size: 1rem;
    font-weight: 600;
    color: #002d40;
    box-shadow: -2px 4px 8px rgba(0, 0, 0, 0.9);
}

.club-dropdown {
    background: white;
    border: 2px solid transparent; /* Prepare for focus border */
    padding: 12px 40px 12px 20px;
    border-radius: 12px;
    font-weight: 600;
    color: #002d40;
    font-size: 1rem;
    width: 280px;
    cursor: pointer;
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2); /* Softer shadow */
    outline: none;
    appearance: none;
    transition: all 0.3s ease;
    
    /* Custom Arrow */
    background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='%23002d40' stroke-width='3' stroke-linecap='round' stroke-linejoin='round'%3e%3cpolyline points='6 9 12 15 18 9'%3e%3c/polyline%3e%3c/svg%3e");
    background-repeat: no-repeat;
    background-position: right 15px center;
    background-size: 18px;
}

/* Hover and Focus States */
.club-dropdown:hover {
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
}

.club-dropdown:focus {
    border-color: #002d40;
    background-color: #f9f9f9;
}
</style>