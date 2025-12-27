<script setup>

</script>

<template>
  <main>

    <div class="card">
      <div class="logo">
        <img src="@/assets/logo.png" alt="Logo">
      </div>

      <div class="buttons">
        <button @click="studentLogin" class="student-login">Student Login</button>
        <button @click="clubAdmin" class="club-admin">Club Admin</button>
      </div>
    
    </div>

  </main>

</template>

<style scoped>
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

  .card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 500px;
    height: 600px;
    gap: 50px;
    backdrop-filter: blur(5px);
    border-radius: 20px;
    background-color: #ffffff17;
    border: 1px solid rgba(255, 255, 255, 0.12);
  }

  .logo {
    width: 300px;
    height: 300px;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    display: flex;
  }

  .student-login {
    width: 200px;
    height: 50px;
   justify-content: center;
   margin: 0 auto;
   display: flex;
    align-items: center;
    background-color: #214444;
    border: none;
    font-size: 18px;
    color: white;
    font-family: 'Poppins', sans-serif;
    border-radius: 35px;
  }

  .club-admin {
    width: 200px;
    height: 50px;
   justify-content: center;
   margin: 0 auto;
   display: flex;
    align-items: center;
    background-color: #214444;
    border: none;
    font-size: 18px;
    color: white;
    font-family: 'Poppins', sans-serif;
    border-radius: 35px;
  }

  .buttons { 
    display: flex;
    gap: 20px;
    margin-top: 50px;
    align-items: center;
  }

  .student-login:hover {
    background-color: #659399;
    cursor: pointer;
  }

  .club-admin:hover {
    background-color: #659399;
    cursor: pointer;
  }

</style>