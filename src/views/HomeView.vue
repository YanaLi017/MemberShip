<script setup>
import { useRouter } from 'vue-router';
const router = useRouter();
const studentLogin = () => {
  router.push({ name: 'studentlogin' });
};
const clubLogin = () => {
  router.push({ name: 'clublogin' });
};
const signUp = () => {
  router.push({ name: 'signup' });
};
</script>

<template>
  <main>

    <div class="card">
      <div class="logo">
        <img src="@/assets/logo.png" alt="Logo">
      </div>

      <div class="option">
        <div  class="buttons">
          <button @click="studentLogin" id="button">Student Login</button>
          <button @click="clubLogin" id="button">Club Admin</button>
        </div>

        <div class="signup">
          <span>
            Don't have an account? <span ><button @click="signUp" id="signupbtn">Sign up</button></span>
          </span>
        </div>
      </div>


    </div>

  </main>

</template>

<style scoped>
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

.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 500px;
  height: 600px;
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
  display: flex;

}

.option{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 150px;

}

.buttons {
  display: flex;
  gap: 20px;
  align-items: center;
}

#button {
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
.signup{
  padding-top: 10px;
}
.signup span,button{
  font-size: medium;
}

#signupbtn{
  background-color: transparent;
  border: none;
  cursor: pointer;
  color: #214444;
}

#button:hover {
  background-color: #659399;
  cursor: pointer;
}

.club-admin:hover {
  background-color: #659399;
  cursor: pointer;
}
</style>