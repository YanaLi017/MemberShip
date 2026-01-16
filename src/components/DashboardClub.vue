<script setup>
import dateTime from '@/components/Date&time.vue';
import weather from '@/components/Weather.vue';
</script>

<template>
    <!-- Main content -->
    <div class="content">

        <div class="analytics">
            <div class="contmem">
                <h2>Total Members:</h2>
                <p>35</p>
            </div>
            <div class="contmem">
                <h2>New Boarding Today:</h2>
                <p>40</p>
            </div>
            <div class="contmem">
                <h2>Active Projects:</h2>
                <p>2</p>
            </div>
        </div>

        <!-- DateTime & Weather -->
        <div class="date-time">
            <div>
                <dateTime />
            </div>
            <div>
                <weather />
            </div>
        </div>

    </div>
</template>

<style scoped>
.content {
    width: 95%;
    height: 76%;
    margin-top: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.analytics {
    width: 95%;
    height: 30%;
    display: flex;
    align-items: center;
    gap: 50px;
    border-radius: 12px;
    padding: 15px;
}

.contmem {
    width: 30%;
    height: 100%;
    background-color: #C6D8D8;
    backdrop-filter: blur(10px);
    border-radius: 15px;
    border: solid 2px rgba(255, 255, 255, 0.5);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 10px;
}

.analytics h2 {
    font-size: 20px;
    font-weight: 600;
    color: #214444;
}

.analytics p {
    font-size: 30px;
    font-weight: 600;
    color: #214444;
}

.date-time {
    width: 30%;
    height: 20%;
    background-color: rgba(219, 228, 228,0.2);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    border: solid 2px #ffffff;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 40px;
    position: fixed;
    bottom: 350px;
    left: 348px;
}
</style>