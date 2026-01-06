<script setup>
import { useRouter } from 'vue-router';
import { ref } from 'vue';

const router = useRouter();
const login = () => {
    router.push({ name: 'home' });
};

const password = ref('');
const showPassword = ref(false); // Controls the visibility
</script>

<template>
    <main>
        <div class="student-card">

            <div>
                <img src="@/assets/logo.png" alt="Logo">
            </div>

            <div class="title">
                <h1>Create Your Account</h1>
            </div>

            <div class="student-form">
                <input type="text" placeholder="Full Name">
                <input type="text" placeholder="Student ID">
            </div>

            <div class="student-form">
                <input type="text" placeholder="Program">
                <input type="text" placeholder="Campus">
            </div>

            <div class="student-form">
                <input type="text" placeholder="Year Level">
                <input type="text" placeholder="Section">
            </div>

            <div class="student-form">
                <input type="text" placeholder="Email">
                <div class="input-container">
                    <input :type="showPassword ? 'text' : 'password'" id="password" v-model="password"
                        placeholder="Password">
                    <button type="button" @click="showPassword = !showPassword" class="toggle-btn">
                        <svg v-if="!showPassword" class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true"
                            xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                            <path stroke="currentColor" stroke-width="2"
                                d="M21 12c0 1.2-4.03 6-9 6s-9-4.8-9-6c0-1.2 4.03-6 9-6s9 4.8 9 6Z" />
                            <path stroke="currentColor" stroke-width="2" d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
                        </svg>

                        <svg v-else class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true"
                            xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M3.933 13.909A4.357 4.357 0 0 1 3 12c0-1 4-6 9-6m7.6 3.8A5.068 5.068 0 0 1 21 12c0 1-3 6-9 6-.314 0-.62-.014-.918-.04M5 19 19 5m-4 7a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
                        </svg>


                    </button>
                </div>
            </div>

            <div class="signup">
                <button id="signupBtn">Join the MemberShip </button>
                <span>Already have an account? <button id="" @click="login">Login</button></span>
            </div>
        </div>
    </main>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
    font-family: 'Poppins', sans-serif;
}

main {
    background-image: url('@/assets/bg .jpg');
    width: 100dvw;
    height: 100dvh;
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;
}

.student-card {
    width: 50rem;
    height: 40rem;
    background-color: rgba(255, 255, 255, 0.4);
    backdrop-filter: blur(5px);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-radius: 20px;
}


.title h1 {
    font-size: 30px;
    font-weight: 600;
    color: #214444;
}

.student-form {
    display: flex;
    gap: 50px;
    margin-top: 15px;
}

input {
    width: 300px;
    height: 40px;
    border-radius: 30px;
    border: none;
    padding: 20px;
    font-size: 15px;
}

.signup {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
    gap: 10px;
}

#signupBtn {
    width: 300px;
    height: 50px;
    border-radius: 30px;
    border: none;
    background-color: #214444;
    color: white;
    font-size: 20px;
    cursor: pointer;
}

#signupBtn:hover {
    background-color: #659399;
}

button {
    background-color: transparent;
    border: none;
    color: #214444;
    cursor: pointer;
    font-size: 15px;
}

.input-container {
  position: relative;
  display: flex;
  align-items: center;
}

.toggle-btn {
  margin-top: 5px;
  position: absolute;
  right: 5px;
  background-color: transparent;
  border: none;
  cursor: pointer;
}
</style>