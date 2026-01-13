<script setup>
import { ref, onMounted } from 'vue';

const studentId = ref('');
const program = ref('');
const campus = ref('');
const yearLevel = ref('');
const section = ref('');
const email = ref('');
onMounted(() => {
    const savedName = localStorage.getItem('loggedStudentName');
    if (savedName) {
        fullName.value = savedName;
    }
});


const fullName = ref('Student'); // Default value if nothing is found

onMounted(() => {
    const savedName = localStorage.getItem('loggedStudentName');
    const savedStudentId = localStorage.getItem('loggedStudentId');
    const savedProgram = localStorage.getItem('loggedStudentProgram');
    const savedCampus = localStorage.getItem('loggedStudentCampus');
    const savedYearLevel = localStorage.getItem('loggedStudentYearLevel');
    const savedSection = localStorage.getItem('loggedStudentSection');
    const savedEmail = localStorage.getItem('loggedStudentEmail');

    if (savedName) fullName.value = savedName;
    if (savedStudentId) studentId.value = savedStudentId;
    if (savedProgram) program.value = savedProgram;
    if (savedCampus) campus.value = savedCampus;
    if (savedYearLevel) yearLevel.value = savedYearLevel;
    if (savedSection) section.value = savedSection;
    if (savedEmail) email.value = savedEmail;
});
</script>
<template>
    <div class="content">

        <div class="settings-card">
            <h1>Login Credentials</h1>

            <div class="info">
                <div class="items">
                    <label for="">Student Name:</label>
                    <input type="text" name="" id="" :placeholder="fullName" readonly="">
                </div>
                <div class="items">
                    <label for="">Student ID:</label>
                    <input type="text" name="" id="" :placeholder="studentId" readonly="">
                </div>
            </div>
            <div class="info">
                <div class="items">
                    <label for="">Program:</label>
                    <input type="text" name="" id="" :placeholder="program" readonly="">
                </div>
                <div class="items">
                    <label for="">Campus:</label>
                    <input type="text" name="" id="" :placeholder="fullName" readonly="">
                </div>
            </div>
        </div>

    </div>
</template>

<style scoped>
*{
    font-family: 'Poppins', sans-serif;
}
.content {
    width: 95%;
    height: auto;
    margin-top: 150px;
    display: flex;
    align-items: center;
}

.settings-card {
    width: 100%;
    height: 100%;
    background-color: rgb(33, 68, 68, 0.4);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    padding: 20px;
    display: flex;
    flex-direction: column;
}

h1 {
    text-align: left;
    font-weight: 600;
}

.info {
    width: 100%;
    display: flex;
    padding: 10px;
    gap: 100px;
    
}
.items{
    width: 40%;
    display: flex;
    font-size: 22px;
    justify-content: space-between;
}

.items label {
    color: #ffffff;
    font-weight: 600;
}
.items input{
    outline: none;
    padding: 2px 10px;
    font-size: 18px;
    border-radius: 16px;
    width: 300px;
    border: none;
}
</style>